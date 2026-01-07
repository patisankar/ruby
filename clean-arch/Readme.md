# Rails Anti-Patterns → Clean Architecture Alternatives

## 1. Fat ActiveRecord Models as the “Domain”
**Anti-pattern**
- `ApplicationRecord` models contain validations, business rules, billing logic, emails, permissions, and reporting.

**Problem**
- Business logic is tightly coupled to persistence and Rails lifecycle.
- Difficult to unit test without the database.

**Clean Alternative**
- Treat ActiveRecord models as **infrastructure/persistence models**.
- Move business rules into **domain entities and value objects (POROs)**.
- Orchestrate behavior via **application use cases**.

---

## 2. Callbacks Performing Side Effects
**Anti-pattern**
- `after_create` or `after_commit` callbacks sending emails, enqueueing jobs, or calling APIs.

**Problem**
- Side effects are implicit and hard to reason about.
- Callbacks execute in unexpected contexts (seeds, console, tests).

**Clean Alternative**
- Move side effects into **use cases**.
- Optionally publish domain events from the use case and handle them in outer layers.

---

## 3. Controllers Containing Business Logic
**Anti-pattern**
- Controllers managing transactions, branching logic, and multi-step workflows.

**Problem**
- Business rules become HTTP-coupled.
- Poor reuse across jobs, CLI, or other entry points.

**Clean Alternative**
- Controllers act as **interface adapters**:
  - Parse/validate input
  - Invoke a use case
  - Render output

---

## 4. Generic “Service Objects”
**Anti-pattern**
- Large, vague `*_service.rb` classes with many unrelated methods.

**Problem**
- Becomes a second “fat model” with unclear responsibilities.

**Clean Alternative**
- Create **use-case-specific classes**:
  - `RegisterUser`
  - `ApproveInvoice`
- One public method (`call`), explicit dependencies.

---

## 5. ActiveRecord Scopes as Business Rules
**Anti-pattern**
- Business meaning embedded in SQL scopes.

**Problem**
- Rules are tied to database and difficult to test independently.

**Clean Alternative**
- Express business rules in **domain entities or policies**.
- Use scopes only for query optimization.

---

## 6. Scattered Authorization Logic
**Anti-pattern**
- Authorization checks duplicated across controllers, models, and views.

**Problem**
- Inconsistent enforcement and security drift.

**Clean Alternative**
- Perform workflow-level authorization in the **use case** or **domain policy**.
- Controllers pass the current actor explicitly.

---

## 7. Globals in Business Logic
**Anti-pattern**
- Direct usage of `Time.current`, `SecureRandom`, `Rails.env`, or `Current.user`.

**Problem**
- Non-deterministic behavior and brittle tests.

**Clean Alternative**
- Inject collaborators (clock, ID generator, actor).
- Pass dependencies explicitly.

---

## 8. Database Constraints as the Only Validation
**Anti-pattern**
- Relying solely on DB constraints for business rules.

**Problem**
- Business rules are invisible and errors occur late.

**Clean Alternative**
- Enforce invariants in **domain entities/use cases**.
- Keep DB constraints as a safety net.

---

## 9. Direct Dependency on External APIs
**Anti-pattern**
- Calling Stripe, Twilio, etc., directly from controllers or models.

**Problem**
- Vendor lock-in and poor testability.

**Clean Alternative**
- Define **ports (interfaces)** in the application layer.
- Implement adapters in infrastructure.

---

## 10. Background Jobs Duplicating Logic
**Anti-pattern**
- Jobs re-implement business workflows already in controllers.

**Problem**
- Divergent behavior over time.

**Clean Alternative**
- Jobs act as adapters that invoke the same **use cases**.

---

## 11. Serializers Containing Business Decisions
**Anti-pattern**
- Serializers computing eligibility, pricing, or state transitions.

**Problem**
- Business logic tied to presentation.

**Clean Alternative**
- Use cases return **result DTOs** with decisions made.
- Serializers only format output.

---

## 12. Hidden or Inconsistent Transaction Boundaries
**Anti-pattern**
- Transactions buried in models, callbacks, or utilities.

**Problem**
- Partial writes and race conditions.

**Clean Alternative**
- The **use case** defines the transaction boundary.
- Repositories handle persistence details.

---

## Summary Mapping

**Outer Layers (Rails)**
- Controllers, Jobs, Mailers, Views, ActiveRecord, External Clients

**Inner Layers (Clean Core)**
- Domain entities, value objects, policies
- Application use cases and ports

Clean Architecture in Rails is about **explicit boundaries, inward dependencies, and business-first design**.
