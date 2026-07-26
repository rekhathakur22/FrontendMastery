# Module 1 — JavaScript Fundamentals

## JavaScript Introductio
- what is Javascript ?
- History
- Why JavaScript was created
- ECMAScript
- JavaScript Engines
- V8 Engine
- SpiderMonkey
- JavaScript Runtime

## How JavaScript Works
- Parsing
- AST
- Compilation
- Interpretation
- Just-In-Time Compilation
- Execution

## Execution Context

- Global Execution Context
- Function Execution Context
- Creation Phase
- Execution Phase
- Variable Environment
- Lexical Environment
- this Binding

## Memory
- Stack Memory
- Heap Memory
- Primitive vs Reference values

## Variables
- var
- let
- const

### Understand (important topic)
- Scope
- Hoisting
- Temporal Dead Zone
- Redeclaration
- Reassignment

## Data Types

### Primitive

- Number
- String
- Boolean
- Null
- Undefined
- Symbol
- BigInt

### Reference

- Object
- Array
- Function

##  Type Conversion
### Implicit
```js
==
```
### explicit
```js
Number()

String()

Boolean()
```

## Operators
- Arithmetic
- Comparison
- Logical
- Assignment
- Bitwise
- Spread
- Rest
- Optional Chaining
- Nullish Coalescing


# Module 2 — Scope & Closures
## Scope
- Global Scope
- Function Scope
- Block Scope
- Lexical Scope
- Nested Scope
- Scope Chain
## Closure

undserstand

Outer Function

↓

Inner Function

↓

Remembers Variables

### Questions
- Why closures work
- Memory implications
- Private variables
- Interview examples

# Module 3 — Functions
- Function Declaration
- Function Expression
- Arrow Function
- Anonymous Function
- Named Function
- Immediately Invoked Function (IIFE)
- Higher Order Function
- Callback Function
- Pure Function
- Impure Function
- Recursive Function
- Generator Function

## this Keyword
- Global
- Function
- Method
- Arrow Function
- Constructor Function
- call()
- apply()
- bind()

# Module 4 — Objects
- Object Literals
- Property Access
- Descriptors
- Object.freeze()
- Object.seal()
- Object.preventExtensions()

## Prototype
- Prototype Chain
- proto
- prototype
- Inheritance
- Delegation

## Classes
- Constructor
- Methods
- Inheritance
- super
- Static Methods
- Private Fields

# Module 5 — Arrays
## Methods
push
pop
shift
unshift
slice
splice
concat
flat
flatMap
find
findIndex
some
every
filter
map
reduce
sort
reverse
fill
copyWithin
entries
keys
values

* Time Complexity
* Mutating vs Non-Mutating methods

# Module 6 — Strings
- trim
- replace
- replaceAll
- includes
- startsWith
- endsWith
- slice
- substring
- split
- repeat
- padStart
- padEnd

# Module 7 — Numbers
- Number object
- Math object
- Random
- Rounding
- Precision
- NaN
- Infinity

# Module 8 — Error Handling
- try
- catch
- finally
- throw
- Custom Errors

# Module 9 — Asynchronous JavaScript
### Call Stack
```js
main()

↓

function()

↓

return
```
### Web APIs
- Timer
- DOM
- Fetch
- Console
- Storage

### Callback Queue
### Event Loop
- setTimeout()
- Promise
- queueMicrotask()
- async
- await
> Execution order

### promises
- States
- Pending
- Fulfilled
- Rejected
- then
- catch
- finally
- Promise.all()
- Promise.allSettled()
- Promise.any()
- Promise.race()

### Async Await
- Why it exists
- How it works
- Error handling
- Sequential execution
- Parallel execution

# Module 10 — DOM
- DOM Tree
- Selection
- Traversal
- Modification
- Creation
- Deletion
- Cloning
- Events
- Event Bubbling
- Capturing
- Delegation
- Forms
- Validation

# Module 11 — Browser Storage
- Cookies
- Session Storage
- Local Storage
- IndexedDB

# Module 12 — Modules
- ES Modules
- import
- export
- default export
- named export
- Dynamic import

# Module 13 — Advanced JavaScript
- Destructuring
- Spread
- Rest
- Template Literals
- Tagged Templates
- Optional Chaining
- Nullish Coalescing
- Short Circuiting
- Object Shorthand
- Computed Properties
- Symbols
- Iterators
- Generators
- Map
- Set
- WeakMap
- WeakSet
- Proxy
- Reflect

# Module 14 — Functional Programming
- Immutability
- Pure Functions
- Composition
- Currying
- Memoization
- Debouncing
- Throttling

# Module 15 — OOP
- Encapsulation
- Abstraction
- Inheritance
- Polymorphism
- SOLID basics

# Module 16 — Performance
- Memory Leak
- Garbage Collection
- Reflow
- Repaint
- Layout Thrashing
- Lazy Loading
- Code Splitting
- Tree Shaking

# Module 17 — JavaScript in Browser
Rendering Pipeline
Critical Rendering Path
Script Loading
defer
async
module
DOMContentLoaded
load

# Module 18 — Networking

- HTTP
- HTTPS
- REST APIs
- JSON
- AJAX
- Fetch API
- Headers
- Methods
- Status Codes
- CORS
- Authentication
- JWT basics

# Module 19 — Design Patterns

- Module Pattern
- Factory Pattern
- Singleton
- Observer
- Publisher Subscriber
- Constructor Pattern
- Prototype Pattern
- MVC basics

# Module 20 — Modern JavaScript

- ES6
- ES2017
- ES2018
- ES2019
- ES2020
- ES2021
- ES2022
- ES2023+

# Module 21 — Interview Coding

Implement from scratch

- map()
- filter()
- reduce()
- bind()
- call()
- apply()
- debounce()
- throttle()
- promiseAll()
- deepClone()
- flattenArray()
- curry()
- memoize()
- eventEmitter()

# Module 22 — Machine Coding

Build these without watching tutorials:

- Calculator
- Todo App
- Weather App
- Infinite Scroll
- Image Carousel
- Search Autocomplete
- Kanban Board
- Drag & Drop
- File Explorer
- Infinite Pagination
- Chat UI
- Notes App

# Module 23 — JavaScript Interview Questions

Practice questions on:

- Hoisting
- Closures
- Scope
- Execution Context
- Event Loop
- Promises
- Async/Await
- Prototype
- this
- Objects
- Arrays
- Event Delegation
- Debouncing & Throttling
- Memory Leaks
- Garbage Collection
- Modules
- ES6+

> Aim to solve 300–500 conceptual questions, not just coding questions.

# Module 24 — Source Code Reading

Read real-world JavaScript code from:

- React
- Redux Toolkit
- Axios
- Lodash
- Day.js
- Zustand



# Module 25 — Final Interview Preparation

Review everything through a structured process:

- Explain every concept without notes.
- Draw diagrams for execution context, scope chain, prototype chain, and the - event loop.
- Implement common polyfills from memory.
- Build at least 10–15 projects with increasing complexity.
- Practice 100+ JavaScript coding problems (arrays, strings, objects, - recursion, promises, DOM).
- Take mock interviews and time yourself explaining answers aloud.
```js 
1. JavaScript Basics
2. Execution Context
3. Memory
4. Variables & Hoisting
5. Scope
6. Closures
7. Functions
8. this Keyword
9. Objects
10. Prototype
11. Arrays
12. Strings
13. Error Handling
14. Event Loop
15. Promises
16. Async/Await
17. DOM
18. Browser APIs
19. ES6+
20. Functional Programming
21. OOP
22. Performance
23. Networking
24. Design Patterns
25. Polyfills
26. Machine Coding
27. Interview Revision
```

One suggestion for your learning style

From our recent conversations, I know you're building a Frontend Mastery repository and you prefer learning concepts deeply rather than memorizing syntax. A great way to structure this is to create one Markdown file for every topic (for example, Execution Context.md, Closures.md, Event Loop.md) using a consistent template:
 
- What is it?
- Why was it introduced?
- How does it work internally?
- Visual diagram
- Syntax
- Real-world examples
- Common interview questions
- Common mistakes
- Best practices
- Coding exercises
- Mini project
- Key takeaways

That approach will give you a repository that doubles as your personal interview handbook.