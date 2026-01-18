
### Why
Before stimulas, it is very slow load full page HTML, 

To address this, It is progressive enhancement, it apply the external JS Event handler.  It also maintains the separation of concerns that has been lost in many contemporary JavaScript frameworks.
It manipulate existing HTML, hiding, changing CSS.

It also maintains the separation of concerns that has been lost in many contemporary JavaScript frameworks.

Stimulus to create new DOM elements, and you’re definitely free to do that. We might even add some sugar to make it easier in the future. But it’s the minority use case. The focus is on manipulating, not creating elements.
 

```ruby
<div data-controller="clipboard">
  PIN: <input data-clipboard-target="source" type="text" value="1234" readonly>
  <button data-action="clipboard#copy">Copy to Clipboard</button>
</div>
```
### How it different than other JS framework
State is stored in the HTML, so that controllers can be discarded between page changes, but still reinitialize as they were when the cached HTML appears again. It really is a remarkably different paradigm. Like React + Redux then turbo + Stimulas
Stimulus is designed to enhance static or server-rendered HTML—the “HTML you already have”—by connecting JavaScript objects to elements on the page using simple annotations.

