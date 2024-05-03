# Episode 3 : Hoisting

```javascript
// code example 1

var x = 7;

function getName() {
  console.log('Namaste JavaScript');
}

getName();
console.log(x);
```

Output:

> Namaste JavaScript

> 7

```javascript
// code example 2

getName(); // in most languages, both lines which are above their declaration will give error. Not in JS though.
console.log(x);

var x = 7;

function getName() {
  console.log('Namaste JavaScript');
}
```

Output:

> Namaste JavaScript

> undefined

```javascript
// code example 3

getName();
console.log(x);

function getName() {
  console.log('Namaste JavaScript');
}
```

Output:

> Namaste JavaScript

> Error: x is not defined // note that not defined here and "undefined" in
> sample 2 are totally different.

- Not defined: "Not defined" typically refers to a situation where a variable has been used without being declared at all in the entire code and also not in the memory space. This would result in a reference error because the variable doesn't exist in the current scope or context.

- Undefined: It is a placeholder that is assigned to a variable by the
  Javascript Engine until the variable is assigned with some other value. Also, "Undefined" refers to a variable that has been declared but has not been assigned a value. In this case, the variable exists, but it hasn't been given a specific value yet, so its value is undefined.

**Hoisting** in JavaScript is a concept where variable and function declarations are moved to the top of their containing scope during the initial memory creation phase/parsing/skimming of the code, allowing them to be accessed before their formal declaration in the code. During this process, memory space is allocated for variables and functions.However, only the declarations themselves are hoisted, not their initializations or values.

```javascript
// code example 4

function getName() {
  console.log('Namaste JavaScript');
}

console.log(getName);
```

Output:

> f getName(){

>      console.log("Namaste JavaScript");

> }

```javascript
// code example 5

getName();
console.log(x);
console.log(getName);

var x = 7;

function getName() {
  console.log('Namaste JavaScript');
}
```

Output:

> Namaste JavaScript

> undefined

> f getName(){

>      console.log("Namaste JavaScript);

> }

```javascript
// code example 6

console.log(getName);
console.log(getName2);
console.log(getName3);

var getName3 = function () {
  console.log('Namaste JavaScript');
};

var getName2 = () => {
  // use fat arrow function
  console.log('Namaste JavaScript');
};

function getName() {
  console.log('Namaste JavaScript');
}
```

Output:

> f getName(){

>      console.log("Namaste JavaScript);

> }

> undefined //it is because getname2 behaves as variable and not function.

> undefined //it is because getname3 behaves as variable and not function.

---

**REASON OF WEIRDNESS**

- The answer lies in the Global Exection Context. In the memory phase, the
  variables will be initialized as _undefined_ and functions will get the whole
  function code in their memory.

- This is the reason why we are getting these outputs.

```javascript
// code example 7 - Call Stack demo example (how call stack is popping in and popping out)

var x = 7;

function getName() {
  console.log('Namaste JavaScript');
}

getName();
console.log(x);
console.log(getName);
```
