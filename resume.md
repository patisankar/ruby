# Shankar [Last Name]
Senior Software Engineer – Ruby on Rails  
[City, State] • [LinkedIn] • [GitHub] • [Email]

---

## SUMMARY

Senior Software Engineer with 10+ years of experience building, scaling, and modernizing Ruby on Rails applications. Proven ability to design maintainable architectures, reason deeply about Ruby and Rails internals, and deliver data-driven internal tools used by engineers and data scientists. Strong collaborator with a track record of leading through ambiguity, prioritizing correctness and performance, and enabling safe iteration in production systems.

---

## CORE TECHNICAL SKILLS

**Languages & Frameworks**
- Ruby, Ruby on Rails (10+ years)
- SQL (PostgreSQL), ActiveRecord
- JavaScript, HTML, CSS
- Stimulus, Turbo (Hotwire)

**Ruby & Rails Internals**
- Ruby object model, method lookup chain (`include`, `prepend`, `extend`)
- Singleton classes and metaprogramming trade-offs
- Garbage collection (generational GC, allocation awareness)
- Concurrency (threads, processes, GIL implications)
- Rails request lifecycle and ActiveRecord internals

**Architecture & Systems**
- Modular monolith design
- Service objects vs callbacks
- Background jobs (Sidekiq)
- Feature flags and safe rollouts
- Observability and production debugging

**Testing & Quality**
- RSpec / Minitest
- Unit, integration, and system tests
- Characterization tests for legacy systems
- Test-driven and experiment-driven development

---

## PROFESSIONAL EXPERIENCE

### Senior Software Engineer — Ruby on Rails  
**[Company Name]** | [Dates]

- Led the design and evolution of a large-scale payment gateway built on Ruby on Rails, supporting business-critical transaction processing.
- Made architectural decisions under ambiguity by favoring reversible designs, including migrating from a tightly coupled monolith toward a modular monolith with clear domain boundaries.
- Designed and implemented service-object–based workflows to replace implicit ActiveRecord callbacks, improving clarity, testability, and operational safety.
- Optimized ActiveRecord performance by eliminating N+1 queries, introducing appropriate indexing strategies, and batching large data operations.
- Built and operated background job pipelines using Sidekiq, with a focus on idempotency, retry safety, and observability.
- Implemented percentage-based feature flags and gradual rollout strategies to reduce blast radius and enable data-driven experimentation in production.
- Worked extensively with both structured (transactional) and unstructured (logs, events, JSON payloads) data, balancing schema stability with flexibility.
- Diagnosed and resolved complex production issues through systematic debugging, metrics analysis, and collaboration across teams.
- Mentored engineers through code reviews and design discussions, emphasizing maintainability over clever abstractions.
- Collaborated closely with product managers, designers, and data stakeholders to translate ambiguous requirements into incremental, shippable solutions.

---

## SELECTED PROJECTS

### Internal Quality Evaluation Tool (Rails POC)
- Designed and built a Ruby on Rails application to help engineers and data scientists evaluate feature quality and iterate using real data.
- Modeled evaluation runs, datasets, and results using a mix of relational schemas and JSONB for evolving data.
- Implemented asynchronous evaluation and aggregation using Sidekiq.
- Built server-rendered dashboards with Rails views enhanced by Stimulus for lightweight interactivity.
- Used metrics and usage data to guide iteration and validate product decisions.

---

## TESTING & QUALITY PRACTICES

- Write tests to protect core invariants, enable refactoring, and support experimentation.
- Prefer explicit, behavior-focused tests over brittle implementation tests.
- Use characterization tests to safely refactor legacy code under unclear requirements.
- Balance coverage with signal to maintain fast feedback loops.

---

## COLLABORATION & LEADERSHIP

- Comfortable leading without formal authority by aligning stakeholders, documenting trade-offs, and guiding teams through ambiguous technical decisions.
- Communicate complex technical concepts clearly to engineers, product partners, and leadership.
- Treat internal users as customers and iterate based on feedback and data.

---

## EDUCATION

**[Degree]**, [Field of Study]  
[University Name]

---

## OPTIONAL

- RailsConf / RubyConf attendee (talks on Rails at scale, modular monoliths, safe rollouts)
- Open-source contributions or internal libraries (if applicable)

---
