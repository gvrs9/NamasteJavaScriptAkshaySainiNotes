# Episode 1 : Execution Context

### Everything in JS happens inside the execution context.

Assume execution context to be a big box where everything takes place. It has 2 components in it:

<li> <strong>Memory : </strong>The place where all the variables and functions are stored as (key:value) pairs. Memory component is also known as <em>variable environment</em>.
<li> <strong>Code : </strong>The place where code is executed one line at a time. Code component is also known as <em>Thread of Execution</em>

### JS is a synchronous single-threaded language.

<li> By single threaded, we mean JS can only run 1 command at a time
<li> By synchronous single threaded, we mean it can run 1 command at a time, <em>in a specific order</em>

### JS is a High-Level, Single-Threaded, Garbage Collected, Interpreted or Just In Time Compiled, Prototype based, Multi-Paradigm, Dynamic & Loosely Typed Language, with a Non-Blocking Event Loop!!

<li> <strong>High-Level : </strong>JavaScript is a high-level language, meaning it abstracts away many low-level details like memory management and CPU operations.

<li> <strong>Single-Threaded : </strong>JavaScript is single-threaded, meaning it executes one task at a time. This can lead to some concurrency challenges but also simplifies programming in many cases.

<li> <strong>Garbage Collected : </strong>JavaScript employs automatic memory management through garbage collection, freeing developers from manual memory allocation and deallocation.

<li> <strong>Interpreted or Just In Time Compiled : </strong>JavaScript can be both interpreted and Just-In-Time (JIT) compiled. Interpreted means code is executed line by line, while JIT compilation involves converting JavaScript code into machine code at runtime for improved performance.

<li> <strong>Prototype-based : </strong>JavaScript is prototype-based, meaning objects can inherit properties directly from other objects.

<li> <strong>Multi-Paradigm : </strong>JavaScript supports multiple programming paradigms, including procedural, object-oriented, and functional programming.

<li> <strong>Dynamic & Loosely Typed : </strong>JavaScript is dynamically typed, allowing variables to hold values of any data type. It's also loosely typed, meaning type coercion can occur implicitly.

<li> <strong>Non-Blocking Event Loop : </strong>JavaScript's event loop enables non-blocking asynchronous execution, crucial for handling I/O operations efficiently in web browsers and Node.js.
