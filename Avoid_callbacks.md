Callbacks can behave badly with threads because ActiveRecord connections are per-thread, transactions don’t cross threads, and model instances aren’t safe to share. I avoid doing complex side effects in callbacks and prefer after_commit to enqueue idempotent background jobs, with explicit data passed through

Debugging Challenges: Tracking when callbacks are triggered becomes difficult, especially with associations and implicit saves:

https://www.youtube.com/watch?v=y4e_sXubhyI
