# Stop Overusing Classes: Records, Structs, and Rethinking Inheritance

One pattern I’ve consistently observed in large codebases is this:

We default to classes and inheritance, even when the problem doesn’t need them.

This often leads to:

Deep class hierarchies
Abstract base classes with little real value
Data models treated as if they have behavior

But if we pause and ask a simpler question:

Is this object actually doing anything, or is it just carrying data?

The design often becomes much clearer.

**When It’s Just Data
**
If your model is primarily a data carrier:

No meaningful behavior
No lifecycle
No identity beyond its values

Then a full class is usually overkill.

A better fit:

Java → Records
Ruby → Structs (or simple objects)
record User(String name, int age) {}

This is more than syntactic sugar—it clearly communicates intent:

This is just data.

Where Inheritance Goes Wrong

Inheritance and abstract classes are powerful—but often misused.

Common anti-patterns:

Abstract classes created just to share fields
Hierarchies without real behavioral differences
Premature generalization (“we might need this later”)

Example:

abstract class BaseUser {
    String name;
    int age;
}

If there’s no shared behavior, this abstraction adds complexity without value.

**When Inheritance Actually Makes Sense**

Use inheritance (or interfaces) when you have:

Shared behavior, not just shared structure

Polymorphism (different implementations of the same contract)

A stable abstraction that won’t constantly change


Even then, a good rule of thumb:

Prefer composition over inheritance unless the relationship is truly hierarchical.

The Shift in Thinking

Traditionally:

Java → Everything is a class

Ruby → Flexible, behavior-first
**
Now:**

Java is evolving (Records, pattern matching, etc.)

Encouraging more intent-driven design

Reducing unnecessary ceremony

Practical Heuristic

Data only? → Record (Java) / Struct (Ruby)

Some behavior? → Plain class, keep it simple
Shared behavior across types? → Composition first
True polymorphism? → Then inheritance/interfaces
