
# JavaScript Fundamentals - Interview Notes

> Beginner to Advanced • Interview Ready

---

# Table of Contents

1. What is JavaScript?
2. History of JavaScript
3. Why JavaScript Was Created
4. ECMAScript
5. JavaScript Engines
6. V8 Engine
7. SpiderMonkey
8. JavaScript Runtime
9. Interview Questions

---

# 1. What is JavaScript?

## Definition

JavaScript is a **high-level, dynamically typed, multi-paradigm programming language** primarily used to add **behavior, logic, and interactivity** to web applications.

Originally it ran only in browsers. Today it also runs on servers (Node.js), desktop apps, mobile apps, and more.

## HTML + CSS + JavaScript

| Technology | Responsibility |
|------------|----------------|
| HTML | Structure |
| CSS | Styling |
| JavaScript | Behavior & Logic |

Example:

```html
<button onclick="hello()">Click</button>

<script>
function hello() {
    alert("Hello");
}
</script>
```

---

## Features

- Dynamic typing
- Object-oriented
- Functional programming support
- Event-driven
- Single-threaded
- Asynchronous programming

---

## Interview Definition

> JavaScript is a high-level, dynamically typed programming language used to build interactive web applications. It follows the ECMAScript specification and runs inside JavaScript engines such as V8 and SpiderMonkey.

---

# 2. History of JavaScript

## Before JavaScript

Early websites were static.

Every button click required a request to the server.

Problems:

- Slow
- Poor user experience
- High server load

---

## 1995

Brendan Eich created JavaScript at Netscape.

Time taken:

**10 Days**

---

## Original Names

```
Mocha
 ↓
LiveScript
 ↓
JavaScript
```

The name "JavaScript" was chosen mainly for marketing because Java was very popular.

JavaScript and Java are different languages.

---

## Browser Wars

- Netscape → JavaScript
- Microsoft → JScript

Different implementations caused compatibility issues.

---

## ECMAScript (1997)

ECMA International standardized the language.

JavaScript implementations now follow the ECMAScript specification.

---

## ES6 (2015)

Major release introducing:

- let
- const
- Arrow Functions
- Classes
- Modules
- Promises
- Template Literals

---

## Timeline

```
1995  JavaScript Created
1997  ECMAScript ES1
1999  ES3
2009  ES5
2015  ES6
2016+ Annual Releases
```

---

# 3. Why JavaScript Was Created

Goal:

Bring interactivity to web pages.

Without JavaScript:

```
Click Button
      │
      ▼
Server
      │
      ▼
Reload Entire Page
```

With JavaScript:

```
Click Button
      │
      ▼
JavaScript
      │
      ▼
Update Page Instantly
```

Benefits:

- Client-side validation
- Dynamic UI
- Better UX
- Reduced server requests

---

# 4. ECMAScript

## Definition

ECMAScript is the **official specification (rulebook)** for JavaScript.

It defines:

- Syntax
- Language features
- Behavior

It does **not** execute code.

---

## Analogy

```
Blueprint
    │
    ▼
House
```

Blueprint = ECMAScript

House = JavaScript

---

## ECMAScript vs JavaScript

| ECMAScript | JavaScript |
|------------|------------|
| Specification | Implementation |
| Defines rules | Follows rules |
| Cannot execute code | Executes code through engines |

---

## Interview Answer

> ECMAScript is the language specification, while JavaScript is an implementation of that specification.

---

# 5. JavaScript Engines

## Definition

A JavaScript Engine executes JavaScript code.

Responsibilities:

- Parse
- Create AST
- Compile
- Execute
- Optimize
- Garbage Collection

---

## Popular Engines

| Engine | Browser |
|---------|----------|
| V8 | Chrome / Node.js |
| SpiderMonkey | Firefox |
| JavaScriptCore | Safari |

---

## Execution Pipeline

```
JavaScript
      │
      ▼
Parser
      │
      ▼
AST
      │
      ▼
Compilation
      │
      ▼
Machine Code
      │
      ▼
CPU
```

---

# 6. V8 Engine

Developed by Google.

Used in:

- Chrome
- Node.js
- Chromium browsers

---

## Architecture

```
JavaScript
      │
      ▼
Parser
      │
      ▼
AST
      │
      ▼
Ignition
(Bytecode)
      │
      ▼
Interpreter
      │
      ▼
Runtime Profiling
      │
      ▼
TurboFan
      │
      ▼
Machine Code
      │
      ▼
CPU
```

---

## Components

### Parser

Checks syntax.

### AST

Tree representation of code.

### Ignition

Converts AST into Bytecode.

### Interpreter

Executes Bytecode.

### TurboFan

Optimizes hot code into Machine Code.

### Garbage Collector

Automatically frees unused memory.

---

## Hot Code

Frequently executed code.

TurboFan optimizes only hot code.

---

## Interview Definition

> V8 is Google's high-performance JavaScript engine that parses JavaScript, generates bytecode, interprets it, and compiles frequently executed code into optimized machine code.

---

# 7. SpiderMonkey

Mozilla's JavaScript Engine.

Used in Firefox.

Created by Brendan Eich.

---

## Execution

```
JavaScript
      │
      ▼
Parser
      │
      ▼
AST
      │
      ▼
Interpreter/JIT
      │
      ▼
Machine Code
      │
      ▼
CPU
```

Like V8, it follows ECMAScript.

---

## V8 vs SpiderMonkey

| V8 | SpiderMonkey |
|----|--------------|
| Google | Mozilla |
| Chrome | Firefox |
| Ignition + TurboFan | Baseline JIT + Optimizing JIT |

---

# 8. JavaScript Runtime

## Definition

A JavaScript Runtime is the complete environment required to run JavaScript.

Engine ≠ Runtime

Runtime = Engine + APIs + Event Loop + Memory

---

## Components

```
JavaScript Runtime

├── Engine
├── Memory Heap
├── Call Stack
├── Web APIs / Node APIs
├── Callback Queue
├── Microtask Queue
└── Event Loop
```

---

## Browser Runtime

Provides:

- DOM
- fetch()
- setTimeout()
- localStorage

---

## Node.js Runtime

Provides:

- fs
- http
- path
- crypto

---

## Runtime Flow

```
JavaScript
      │
      ▼
Engine
      │
      ▼
Call Stack
      │
      ▼
Web APIs
      │
      ▼
Queues
      │
      ▼
Event Loop
```

---

# Frequently Asked Interview Questions

## JavaScript

**Q. What is JavaScript?**

JavaScript is a high-level programming language used to create dynamic and interactive applications.

---

## History

**Q. Who created JavaScript?**

Brendan Eich.

**Q. How many days did it take?**

10 days.

**Q. Original names?**

Mocha → LiveScript → JavaScript.

---

## ECMAScript

**Q. Difference between ECMAScript and JavaScript?**

ECMAScript is the specification; JavaScript is its implementation.

---

## Engine

**Q. What is a JavaScript Engine?**

Software that parses, compiles, optimizes, and executes JavaScript.

---

## V8

**Q. What is V8?**

Google's JavaScript engine used by Chrome and Node.js.

---

**Q. What is Ignition?**

V8's bytecode compiler/interpreter component.

---

**Q. What is TurboFan?**

Optimizing compiler that converts hot code into machine code.

---

## SpiderMonkey

**Q. Which browser uses SpiderMonkey?**

Firefox.

---

## Runtime

**Q. What is JavaScript Runtime?**

The complete environment required to execute JavaScript, including the engine, APIs, memory, event loop, and queues.

---

# Quick Revision

- JavaScript → Programming language
- ECMAScript → Specification
- Engine → Executes JavaScript
- V8 → Chrome & Node.js Engine
- SpiderMonkey → Firefox Engine
- Runtime → Complete execution environment
- Ignition → Bytecode
- TurboFan → Machine code
- Hot Code → Frequently executed code
- CPU executes only Machine Code
