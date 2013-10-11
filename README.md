# JavaScript Patterns Slideshow
## Derek Brown

Derek Brown's Presentation - Javascript design patterns
http://dbrown-mn1/~dbrown/patterns

(Note: as a point of posterity, we ran this presentation by pointing the teleconference webcam at Derek's computer screen, because the A/V connector wasn't working. It was rad.)

Great design patterns are reusable, modular expressions of what's going on.

Patterns looked at:
module
singleton
facade
command
factory
observer
delegate

We use Module pattern most at LinkedIn
Pros: Modular (duh), allows private/public encapsulation, clean, readable, less global clutter
Cons: Messy return statement (can be remedied a bit by your approach), unit testing can be difficult, can't easily extend private methods
Used: In almost all of our code

Singleton Pattern
Extension of module + method that ensures a singular instance of the module exists.
Pros: Reduces memory footprint, single point of access, delayed initialization
Cons: Difficult to reset, harder to unit test
Used: Dialog and scroll listener

Facade
Paired with other patterns to provide an extra layer of security/homogenization. Protects properties.
Pros: Easy to implement, works well with other patterns, easy to patch internals, provides simple public interface.
Cons: Cost of implementation vs. value of extra layer of abstraction.
Used: Most of jQuery uses a facade pattern (addClass, sizzle, etc), Typeahead2

Command
Completely separates implementation and execution of methods.
Pros: Decouples implementation from execution, can stack command objects (undo/redo)
Cons: Counter-intuitive to most other patterns, limited use to 'verb-centric' applications, requires protocol
Used: In Venus.js

Factory
Used to create objects, usually belongs to a set or category. Think config pattern, but also returns instance.
Pros: Allows sharing of properties across multiple objects, useful for complex object or components
Cons: Fairly complex, high overhead for garbage collection, unit testing problems
Used: Address book contact factory (java)

Observer
"Pub/sub" stuff, events, callbacks
Pros: Facilitates app-level thinking, removes direct relationships
Cons: No way to know if the other end of the phone is still on the phone (one-way blind), subs unaware of each other
Usage: Events

Delegate
Delegator offloads task to an associated helper object.
Pros: Loose coupling w/o global eventing, easy to maintain structure
Cons: No well-structured way to enforce delegation attachment, assignment occurs prior to initialization
Usage: LI-Backbone

Jimmy: Talk briefly about design patterns of Javascript specifically.
Derek: Not a huge difference between functional and class programming. Biggest difference is overhead of additional functions for encapsulation. (Aside) Bugs can be hard to dissect because of how functional programming works in Javascript, it can be difficult to access.
Jimmy: We should be exposing most internal methods for testing.

Jimmy: If I search design patterns exemplified in other languages, are they translatable to JS?
Derek: Yep, absolutely.
Me: I think the issue I ususally run into is in how other languages handle scoping (like, say for callbacks).
(Everyone agrees and compliments David Drew's hair)