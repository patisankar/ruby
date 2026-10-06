# Introduction
Ruby on Rails is well-suited for building production applications — REST APIs, ActiveRecord models, and background jobs — following its convention-over-configuration approach 

while staying mindful of common pitfalls like N+1 queries, callback overuse, and bloated models. What stands out most about Ruby on Rails is how fast it lets teams ship, which matters a lot for growth-focused products.

## 1. Rails Internals and Production Behavior
- **[Official Rails Guides](https://guides.rubyonrails.org/)**
  Focus on Active Record, caching, Active Job, security, performance, autoloading, and production configuration.
- **[Rails Inside](https://railsinside.com/)**
  Specifically written for senior Rails developers, with emphasis on internals, upgrades, refactoring, and performance.

## 2. Performance and Scalability
- **[Shopify Engineering — How to Write Fast Code in Ruby on Rails](https://shopify.engineering/write-fast-code-ruby-rails)**
  Covers practical Rails performance thinking and measurement.
- **[Shopify — Deconstructing the Monolith](https://shopify.engineering/deconstructing-monolith-designing-software-maximizes-developer-productivity)**
  Useful for senior-level architecture discussions: when to keep a monolith, when to modularize, and when to split services.
- **[Shopify — How Shopify Reduced Storefront Response Times](https://shopify.engineering/how-shopify-reduced-storefront-response-times-rewrite)**
  Good for discussing correctness versus performance in a large Rails system.

## 3. Ruby Internals and Performance
- **[Tender Loving Code / Aaron Patterson](https://tenderlovemaking.com/)**
  Read for Ruby VM behavior, garbage collection, parsing, C extensions, and debugging.
- **[Shopify Ruby Engineering](https://shopify.engineering/search?q=ruby+rails)**
  Focus on YJIT, garbage collection, memory layout, Bootsnap, and concurrency.

## 4. Testing and Maintainable Design
- **[thoughtbot Rails articles](https://thoughtbot.com/blog/tags/ruby-on-rails)**
  Focus on testing strategy, refactoring, object design, and avoiding brittle tests.
- **[Testing Rails](https://books.thoughtbot.com/assets/testing-rails.pdf)**
  Use it as a practical reference for unit, integration, and feature testing.
  
## Best Passionate Ruby Blogs

1. [**Tender Lovemaking — Aaron Patterson**](https://tenderlovemaking.com/)

   Best for Ruby and Rails internals, performance, garbage collection, parsing, debugging, and C extensions. Aaron Patterson is a Ruby and Rails core contributor. This is one of the best sources for senior-level depth.

2. [**Avdi Codes — Avdi Grimm**](https://avdi.codes/)

   Best for object-oriented design, exceptions, refactoring, maintainability, and writing expressive Ruby. His focus is useful for improving PR quality and design judgment.

3. [**RubyTapas**](https://www.rubytapas.com/)

   Short, focused lessons on advanced Ruby, testing, refactoring, and object-oriented design. Good when you have only 15–20 minutes.

4. [**Mike Perham’s Blog**](https://www.mikeperham.com/)

   Very relevant to payment-gateway engineering. Study distributed systems, Sidekiq, background jobs, Redis, concurrency, reliability, and performance.

5. [**Schneems**](https://schneems.com/)

   Excellent for Rails performance, production debugging, open source, memory, and practical engineering lessons.

6. [**Maciej Mensfeld — Running with Ruby**](https://mensfeld.pl/)

   Good for Kafka, Karafka, background processing, Ruby infrastructure, and production systems.

7. [**Andy Croll**](https://andycroll.com/)

   Useful for senior engineering judgment, Rails maintenance, performance, technical leadership, and running mature applications.

8. [**Arkency Blog**](https://blog.arkency.com/)

   Strong source for event sourcing, domain-driven design, CQRS, Ruby design, and complex business workflows.

9. [**Saeloun Blog**](https://blog.saeloun.com/)

   Practical articles about new Ruby and Rails features, performance, database behavior, and Rails upgrades.

10. [**Boring Rails**](https://boringrails.com/)

    Good for production-friendly Rails patterns, maintainability, and simple solutions that scale operationally.


## Rails 8 - archetecture
rails-architecture provides actionable guidance for structuring modern Rails 8 applications, helping developers decide where to place code and which patterns to adopt. 
It compares service objects, concerns, query objects, interactors, POROs, and ActiveRecord relations; recommends folder layouts (app/services, app/queries, app/commands, app/forms, app/policies); and promotes layered design (presentation, application/domain, persistence). Use it when designing feature architecture, refactoring for clarity, splitting responsibilities, choosing between composition vs inheritance, or organizing large monoliths and engines. It includes naming conventions, dependency-injection approaches, testing strategies, anti-pattern warnings (fat models, overused concerns), and migration tips for extracting logic safely. Core value: faster maintainability, clearer ownership boundaries, improved testability, and predictable scaling paths for Rails codebases.

## Rails Blogs
[Rubocop](https://github.com/standardrb/standard?tab=readme-ov-file#running-standards-rules-via-rubocop)


### Ruby on Rails (Official)
- https://rubyonrails.org/blog
- https://medium.com/@angelolumba/ruby-designed-to-make-programmers-happy-d86f12fa9a14
  Official framework updates, security releases, and architectural direction.

### Ruby Inside
- https://rubyinside.com  
  Deep dives into Ruby internals, performance, and language evolution.

### Thoughtbot Blog
- https://thoughtbot.com/blog  
  Excellent content on Rails architecture, refactoring, testing, and engineering culture.

---

## Large-Scale Production Engineering

### Shopify Engineering
- https://shopify.engineering  
  Rails at massive scale: webhooks, background jobs, sharding, performance tuning.

### GitHub Engineering
- https://github.blog/engineering/  
  Scaling Ruby monoliths, reliability, database performance, and observability.

### Stripe Engineering (Payments-Focused)
- https://stripe.com/blog/engineering  
  Payments, APIs, retries, idempotency, and platform reliability.

---

##  Performance, Observability & Internals

### AppSignal Blog
- https://blog.appsignal.com  
  Ruby performance tuning, memory leaks, observability, and monitoring.

### Honeybadger Developer Blog
- https://www.honeybadger.io/blog/  
  Error handling, debugging, and production incident analysis in Rails apps.

### Evil Martians Chronicles
- https://evilmartians.com/chronicles  
  Advanced Ruby, performance optimizations, and modern Rails patterns.

---

## Tier 4: Testing, CI/CD & Code Quality

### Semaphore CI Blog (Ruby)
- https://semaphoreci.com/blog/ruby  
  CI/CD pipelines, testing strategies, and automation for Ruby projects.

### Ruby Weekly
- https://rubyweekly.com  
  Weekly curated Ruby news, libraries, and articles.

---

##  References 
- Shopify Engineering – Webhooks and scale
- Stripe Engineering – Payments, retries, idempotency
- GitHub Engineering – Monoliths at scale
- Thoughtbot – Clean Rails architecture and refactoring



