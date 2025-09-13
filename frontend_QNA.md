
 # HTML 

---

### **1. What are semantic HTML elements? Give examples.**

**Answer:**
Semantic elements clearly describe their meaning in a human- and machine-readable way.

* Example: `<header>`, `<nav>`, `<article>`, `<footer>`
* Non-semantic: `<div>`, `<span>` (don’t tell anything about content).

**Why in interviews:** Helps with SEO, accessibility, and code readability.

---

### **2. Difference between block, inline, and inline-block elements?**

**Answer:**

* **Block:** Takes full width, starts on new line.
  Example: `<div>`, `<p>`, `<h1>`.
* **Inline:** Only takes as much width as content, no new line.
  Example: `<span>`, `<a>`.
* **Inline-block:** Behaves like inline but allows width/height to be set.
  Example: `<button>`.

**Example:**

```html
<div>Block</div>
<span>Inline</span>
<button>Inline-block</button>
```

---

### **3. Difference between `<div>` and `<span>`?**

**Answer:**

* `<div>`: Block-level container, groups larger sections.
* `<span>`: Inline container, used for small parts of text.

**Example:**

```html
<p>This is a <span style="color:red">red word</span> inside a <div>block</div>.</p>
```

---

### **4. What are HTML5 new features?**

**Answer:**
HTML5 introduced:

* Semantic tags (`<header>`, `<footer>`, `<article>`)
* Multimedia (`<audio>`, `<video>`)
* Graphics (`<canvas>`, `<svg>`)
* Storage APIs (`localStorage`, `sessionStorage`)
* Form enhancements (`<input type="date">`, `<input type="email">`).

---

### **5. Difference between HTML and XHTML?**

**Answer:**

* **HTML:** Flexible, forgiving syntax (case-insensitive, unclosed tags allowed).
* **XHTML:** Stricter XML-based, must follow rules (all tags closed, lowercase, attributes quoted).

**Example:**

```html
<!-- HTML -->
<input type=text>

<!-- XHTML -->
<input type="text" />
```


---

### **6. Difference between `id` and `class` in HTML?**

**Explanation:**

* **`id`** → Unique identifier for one element (used once per page).
* **`class`** → Can be applied to multiple elements (used for grouping and styling).

**Interview Tip:**
Use `id` for unique styling or JavaScript targeting, and `class` for reusable styling.

**Example:**

```html
<p id="main-title">Hello World</p>
<p class="highlight">Paragraph 1</p>
<p class="highlight">Paragraph 2</p>
```

Here `id="main-title"` is unique, but multiple elements share `.highlight`.

---

### **7. Difference between relative, absolute, and fixed URLs in HTML?**

**Explanation:**

* **Relative URL** → Path relative to the current page.
* **Absolute URL** → Full path (with domain).
* **Fixed (root-relative) URL** → Starts from root `/` of site.

**Example:**

```html
<!-- Relative -->
<img src="images/pic.png">

<!-- Absolute -->
<img src="https://example.com/images/pic.png">

<!-- Root-relative -->
<img src="/assets/images/pic.png">
```

**Interview Tip:**
Relative is common for internal files, absolute for external resources (like CDN).

---

### **8. What are `data-*` attributes used for?**

**Explanation:**

* Custom attributes to store extra information (metadata) on HTML elements.
* Accessible in JavaScript using `dataset`.

**Example:**

```html
<button data-user-id="42">Click Me</button>

<script>
  const btn = document.querySelector("button");
  console.log(btn.dataset.userId); // "42"
</script>
```

**Interview Tip:**
Used for storing lightweight custom data without polluting HTML structure.

---

### **9. Difference between `<script>`, `<script async>`, and `<script defer>`?**

**Explanation:**

* `<script>` → Blocks HTML parsing until script is loaded & executed.
* `async` → Loads script asynchronously, executes immediately after download.
* `defer` → Loads script in background, executes after HTML is fully parsed.

**Example:**

```html
<!-- Blocking -->
<script src="main.js"></script>

<!-- Async -->
<script src="analytics.js" async></script>

<!-- Defer -->
<script src="app.js" defer></script>
```

**Interview Tip:**

* Use `defer` for most scripts (non-blocking, runs in order).
* Use `async` for independent scripts (like ads, analytics).

---

### **10. Difference between `<link>` and `@import` for including CSS?**

**Explanation:**

* **`<link>`** → HTML way, better performance (parallel loading).
* **`@import`** → CSS way, slower (sequential loading).

**Example:**

```html
<!-- Preferred -->
<link rel="stylesheet" href="style.css">

<!-- Avoid (slower) -->
<style>
  @import url("style.css");
</style>
```

**Interview Tip:**
Always prefer `<link>` for performance.

---

### **11. What are meta tags in HTML?**

**Explanation:**
Meta tags provide metadata (information about the page) to browsers and search engines.

**Common Uses:**

* Charset
* SEO (description, keywords)
* Viewport for responsive design

**Example:**

```html
<meta charset="UTF-8">
<meta name="description" content="Frontend interview prep">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Interview Tip:**
Meta tags affect SEO and responsiveness — very common interview question.

---

### **12. Difference between `<canvas>` and `<svg>`?**

**Explanation:**

* **`<canvas>`** → Pixel-based (bitmap), good for dynamic, high-performance graphics (games).
* **`<svg>`** → Vector-based, scalable without losing quality, good for icons/illustrations.

**Example:**

```html
<!-- Canvas -->
<canvas id="myCanvas" width="100" height="100"></canvas>

<!-- SVG -->
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="blue" />
</svg>
```

**Interview Tip:**
Use **SVG** for static/responsive graphics, **Canvas** for real-time rendering.

---

### **13. Difference between `localStorage`, `sessionStorage`, and `cookies`?**

**Explanation:**

* **localStorage** → Stores data permanently in browser (until cleared).
* **sessionStorage** → Stores data only for one session (tab closes → data lost).
* **cookies** → Small data sent with every HTTP request (can expire, often used for auth).

**Example:**

```js
// localStorage
localStorage.setItem("user", "John");

// sessionStorage
sessionStorage.setItem("theme", "dark");

// cookies
document.cookie = "username=John; expires=Fri, 31 Dec 2025 12:00:00 UTC";
```

**Interview Tip:**
Use `localStorage`/`sessionStorage` for client-only data, `cookies` for server-side communication (auth/session).

---

### **14. What are accessibility (ARIA) attributes? Why important?**

**Explanation:**

* ARIA = Accessible Rich Internet Applications.
* Provide extra info for screen readers (for visually impaired users).
* Make interactive elements accessible.

**Example:**

```html
<button aria-label="Close window">X</button>
<nav aria-label="Main Navigation">...</nav>
```

**Interview Tip:**
Shows awareness of accessibility (a **big plus** in interviews).

---

### **15. Difference between `<section>`, `<article>`, `<aside>`, and `<main>`?**

**Explanation:**

* `<section>` → Thematic grouping of content.
* `<article>` → Self-contained piece (blog post, news).
* `<aside>` → Secondary info (sidebar, ads).
* `<main>` → Main content of the page.

**Example:**

```html
<main>
  <article>
    <h1>Blog Post</h1>
    <p>Content...</p>
  </article>
  <aside>Related posts</aside>
</main>
```

**Interview Tip:**
Using semantic structure improves SEO + accessibility.

---

---

# *CSS Interview Questions (Q16–Q35)**

---

### **16. Difference between relative, absolute, fixed, and sticky positioning?**

**Explanation:**

* **Relative** → Positioned relative to its normal position.
* **Absolute** → Positioned relative to nearest positioned ancestor.
* **Fixed** → Positioned relative to viewport (doesn’t move when scrolling).
* **Sticky** → Acts like relative, but “sticks” to position when scrolling past.

**Example:**

```css
.relative { position: relative; top: 10px; }
.absolute { position: absolute; top: 10px; left: 20px; }
.fixed    { position: fixed; bottom: 0; right: 0; }
.sticky   { position: sticky; top: 0; }
```

**Interview Tip:**
Fixed = navbar always visible, Sticky = header that sticks only after scrolling.

---

### **17. Difference between inline, internal, and external CSS?**

* **Inline:** Inside `style` attribute (highest priority).
* **Internal:** Inside `<style>` tag in `<head>`.
* **External:** Separate `.css` file linked via `<link>`.

**Example:**

```html
<p style="color:red">Inline</p>
<style> p { color: blue; } </style>
<link rel="stylesheet" href="styles.css">
```

**Interview Tip:**
External CSS is preferred for reusability & performance.

---

### **18. Difference between relative units (`%`, `em`, `rem`, `vw`, `vh`)?**

* `%` → Relative to parent element.
* `em` → Relative to parent font-size.
* `rem` → Relative to root font-size (html).
* `vw` / `vh` → Relative to viewport width/height.

**Example:**

```css
.parent { font-size: 20px; }
.child1 { font-size: 2em; }   /* 40px */
.child2 { font-size: 2rem; }  /* relative to <html> font-size */
.box { width: 50vw; height: 50vh; }
```

**Interview Tip:**
Use `rem` for consistency, `%` for fluid layouts.

---

### **19. Difference between absolute, relative, fixed, and sticky positions?**

(Same as Q16 → interviewer may repeat, so explain again clearly).

---

### **20. Difference between Flexbox and CSS Grid?**

* **Flexbox:** 1D layout (row OR column). Best for alignment.
* **Grid:** 2D layout (rows + columns). Best for full page layout.

**Example:**

```css
/* Flexbox */
.container { display: flex; justify-content: center; }

/* Grid */
.container { display: grid; grid-template-columns: 1fr 1fr; }
```

**Interview Tip:**
Flexbox → navbar, Grid → full page structure.

---

### **21. Difference between inline vs block elements in terms of CSS?**

* **Inline:** Respect only horizontal padding/margin, can’t set width/height.
* **Block:** Takes full width, allows all styling.

**Example:**

```html
<span style="width:100px">Inline</span> <!-- won’t work -->
<div style="width:100px">Block</div>
```

---

### **22. What is z-index and how does it work?**

* **z-index** controls stacking order of elements.
* Higher `z-index` = appears on top.
* Only works on positioned elements (`relative`, `absolute`, etc).

**Example:**

```css
.box1 { position: absolute; z-index: 1; }
.box2 { position: absolute; z-index: 2; }
```

---

### **23. Positioning again (relative, absolute, fixed, sticky) with examples**

(Similar to Q16 → interviewer may test with live coding).

---

### **24. Explain the concept of CSS Specificity.**

* Rules determine which CSS applies when conflicts occur.
* Order: Inline > ID > Class/Pseudo-class > Element.

**Example:**

```css
p { color: blue; }        /* low */
p.highlight { color:red;} /* higher */
#special { color:green;}  /* highest */
```

**Interview Tip:**
Be careful with `!important` (overrides everything, avoid overuse).

---

### **25. Difference between `visibility: hidden` and `display: none`?**

* `visibility: hidden` → Element still takes space, just invisible.
* `display: none` → Element removed from layout.

**Example:**

```css
.hidden { visibility: hidden; }
.none { display: none; }
```

---

### **26. Difference between transform, transition, and animation in CSS?**

* **Transform** → Changes element shape/position.
* **Transition** → Smooth change between states.
* **Animation** → Complex sequence of keyframes.

**Example:**

```css
/* Transform */
div { transform: rotate(45deg); }

/* Transition */
div { transition: all 0.5s ease; }

/* Animation */
@keyframes bounce { 0% { top:0; } 50% { top:50px; } }
div { animation: bounce 2s infinite; }
```

---

### **27. Difference between inline CSS vs external CSS in terms of performance?**

* Inline → Faster for very small changes, but bad for maintainability.
* External → Cached by browser, best for performance.

---

### **28. What are pseudo-classes and pseudo-elements?**

* **Pseudo-class** → Defines state (`:hover`, `:focus`).
* **Pseudo-element** → Styles specific part (`::before`, `::after`).

**Example:**

```css
a:hover { color: red; }         /* pseudo-class */
p::first-line { font-weight: bold; } /* pseudo-element */
```

---

### **29. Difference between relative and absolute units (`em`, `rem`, `px`, `%`)?**

(Similar to Q18 → px = fixed, em/rem = scalable, % = relative).

---

### **30. What are media queries and how do they work?**

* Used for **responsive design**.
* Apply styles based on device width/height.

**Example:**

```css
@media (max-width: 600px) {
  body { background: lightblue; }
}
```

---

### **31. Difference between min-width and max-width in responsive design?**

* **min-width** → Styles apply if screen is wider than value (mobile-first).
* **max-width** → Styles apply if screen is smaller than value.

---

### **32. Difference between CSS Grid vs Flexbox? When to use which?**

(Same as Q20 → mention: Grid for 2D, Flexbox for 1D).

---

### **33. Difference between relative path vs absolute path in CSS?**

* **Relative:** Based on current file location.
* **Absolute:** Full path from root or URL.

**Example:**

```css
/* Relative */
background: url("../images/bg.png");

/* Absolute */
background: url("/assets/bg.png");
```

---

### **34. Difference between inline styles and CSS classes in React?**

* **Inline styles:** Written as objects.
* **CSS classes:** External `.css` with `className`.

**Example:**

```jsx
<div style={{color:"red"}}>Inline</div>
<div className="highlight">Class</div>
```

---

### **35. Difference between CSS BEM methodology and normal CSS?**

* **Normal CSS:** Classes can conflict easily.
* **BEM (Block Element Modifier):** Naming convention for scalability.

**Example (BEM):**

```css
.card {}
.card__title {}
.card__title--large {}
```

**Interview Tip:**
BEM shows structured CSS knowledge → often asked in large-scale projects.

---


---

# **JavaScript Interview Questions (Q36–Q45)**

---

### **36. Difference between `var`, `let`, and `const`?**

**Explanation:**

* `var`: Function-scoped, hoisted, can be re-declared.
* `let`: Block-scoped, not hoisted (in temporal dead zone), can be reassigned.
* `const`: Block-scoped, must be initialized, cannot be reassigned.

**Example:**

```js
var x = 1;  
let y = 2;  
const z = 3;  
```

**Interview Tip (say this):**
“In modern JavaScript, we avoid `var` because of hoisting issues. We use `let` for variables that change and `const` for constants or references that don’t change.”

---

### **37. Difference between `==` and `===`?**

**Explanation:**

* `==` → Loose equality, does type conversion.
* `===` → Strict equality, no type conversion.

**Example:**

```js
console.log(5 == "5");   // true (type conversion)
console.log(5 === "5");  // false
```

**Interview Tip:**
“I always prefer `===` because it avoids unexpected type coercion bugs.”

---

### **38. What is hoisting in JavaScript?**

**Explanation:**

* Hoisting = JavaScript moves **declarations** to the top of scope before execution.
* Only declarations are hoisted, not initializations.

**Example:**

```js
console.log(a); // undefined
var a = 5;
```

**Interview Tip:**
“I explain hoisting as: JS remembers variable & function declarations before code runs, but not their values.”

---

### **39. Difference between `null` and `undefined`?**

**Explanation:**

* `null`: Intentional absence of value.
* `undefined`: Variable declared but not assigned.

**Example:**

```js
let x;         // undefined
let y = null;  // null
```

**Interview Tip:**
“In interviews, I say: undefined is system-assigned, null is developer-assigned.”

---

### **40. What is closure in JavaScript?**

**Explanation:**

* A closure is when an inner function remembers variables from its outer function, even after the outer function has finished executing.

**Example:**

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  };
}
const counter = outer();
console.log(counter()); // 1
console.log(counter()); // 2
```

**Interview Tip:**
“I usually explain closure as a way to preserve state in functions. A classic use case is counters or private variables.”

---

### **41. Difference between synchronous and asynchronous JavaScript?**

**Explanation:**

* **Synchronous**: Code executes line by line, blocking next line until finished.
* **Asynchronous**: Code doesn’t block, continues execution, tasks handled later (callbacks, promises).

**Example:**

```js
console.log("Start");
setTimeout(() => console.log("Async task"), 1000);
console.log("End");
```

**Interview Tip:**
“I explain that JS is single-threaded but uses async (callbacks, promises, async/await) to handle non-blocking tasks.”

---

### **42. Difference between event bubbling and event capturing?**

**Explanation:**

* **Bubbling:** Event goes from target → up to ancestors.
* **Capturing:** Event goes from ancestors → down to target.

**Example:**

```js
document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked");
}, false); // bubbling

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
}, true); // capturing
```

**Interview Tip:**
“I mention that bubbling is default and capturing is rarely used but useful for intercepting events earlier.”

---

### **43. Difference between `call`, `apply`, and `bind` methods?**

**Explanation:**

* **call:** Calls function with given `this` and arguments (comma-separated).
* **apply:** Same as `call`, but args as array.
* **bind:** Returns a new function with bound `this`.

**Example:**

```js
function greet(msg) { console.log(msg + " " + this.name); }
const obj = { name: "John" };

greet.call(obj, "Hello");       // Hello John
greet.apply(obj, ["Hi"]);       // Hi John
const bound = greet.bind(obj, "Hey");
bound();                        // Hey John
```

**Interview Tip:**
“I explain: call and apply execute immediately, bind returns a function for later.”

---

### **44. Difference between shallow copy and deep copy in JS?**

**Explanation:**

* **Shallow copy:** Copies top-level, nested objects still reference original.
* **Deep copy:** Complete independent copy.

**Example:**

```js
let obj1 = { a: 1, b: { c: 2 } };
let shallow = {...obj1};
shallow.b.c = 10; // affects obj1

let deep = JSON.parse(JSON.stringify(obj1));
deep.b.c = 20; // doesn’t affect obj1
```

**Interview Tip:**
“I mention that shallow copy is faster but risky, deep copy ensures independence.”

---

### **45. What are promises in JavaScript?**

**Explanation:**

* Promise = object representing a future value (pending, fulfilled, rejected).
* Used for async tasks.

**Example:**

```js
let promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Done"), 1000);
});
promise.then(res => console.log(res));
```

**Interview Tip:**
“I usually explain promise as: a placeholder for a value we don’t have yet, commonly used for API calls.”

---


---

## **JavaScript Interview Questions (Q46–Q65)**

---

### **46. Difference between promise chaining and async/await?**

**Explanation:**

* **Promise chaining**: Use `.then()` to handle sequential async tasks.
* **async/await**: Cleaner syntax, looks synchronous, easier to read.

**Example:**

```js
// Promise chaining
fetch("/data")
  .then(res => res.json())
  .then(data => console.log(data));

// Async/await
async function getData() {
  const res = await fetch("/data");
  const data = await res.json();
  console.log(data);
}
```

**Interview Tip:**
“I’d say async/await is just syntactic sugar over promises — I prefer it for readability.”

---

### **47. Difference between localStorage and sessionStorage?**

**Explanation:**

* **localStorage** → Permanent (until manually cleared).
* **sessionStorage** → Clears when browser/tab is closed.

**Example:**

```js
localStorage.setItem("name", "John");
sessionStorage.setItem("theme", "dark");
```

**Interview Tip:**
“I use localStorage for persistent preferences and sessionStorage for temporary state like tab data.”

---

### **48. Difference between setTimeout and setInterval?**

**Explanation:**

* **setTimeout** → Runs once after delay.
* **setInterval** → Runs repeatedly at intervals.

**Example:**

```js
setTimeout(() => console.log("Run once"), 1000);
setInterval(() => console.log("Repeat"), 1000);
```

**Interview Tip:**
“Use setTimeout for delayed tasks and setInterval for repeated tasks (but clear it to avoid memory leaks).”

---

### **49. Difference between arrow functions and normal functions?**

**Explanation:**

* Arrow functions are shorter and don’t have their own `this`.
* Normal functions bind `this` dynamically.

**Example:**

```js
const obj = {
  name: "John",
  arrow: () => console.log(this.name), // undefined
  normal() { console.log(this.name); } // John
};
obj.arrow();
obj.normal();
```

**Interview Tip:**
“I usually explain arrow functions are great for callbacks, but not for methods needing `this`.”

---

### **50. Difference between for...in and for...of loops?**

**Explanation:**

* **for...in** → Iterates over keys (object properties).
* **for...of** → Iterates over values (arrays, iterables).

**Example:**

```js
let arr = [10, 20, 30];
for (let i in arr) console.log(i);   // 0,1,2
for (let v of arr) console.log(v);   // 10,20,30
```

**Interview Tip:**
“I use for...in for objects and for...of for arrays/iterables.”

---

### **51. Difference between DOM and BOM?**

**Explanation:**

* **DOM**: Document Object Model (HTML structure).
* **BOM**: Browser Object Model (browser features like `window`, `history`).

**Example:**

```js
document.getElementById("id"); // DOM
window.alert("Hello");         // BOM
```

**Interview Tip:**
“I explain DOM = page content, BOM = browser environment.”

---

### **52. Difference between innerHTML and innerText?**

**Explanation:**

* **innerHTML** → Returns HTML (with tags).
* **innerText** → Returns only visible text.

**Example:**

```html
<p id="p"><b>Hello</b> World</p>
<script>
  console.log(p.innerHTML); // <b>Hello</b> World
  console.log(p.innerText); // Hello World
</script>
```

**Interview Tip:**
“innerHTML is powerful but risky (XSS), innerText is safer.”

---

### **53. Difference between event delegation and event handling?**

**Explanation:**

* **Event handling**: Directly attach event to element.
* **Event delegation**: Attach to parent, use bubbling to handle child events.

**Example:**

```js
// Delegation
document.getElementById("list").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") console.log("Clicked", e.target.textContent);
});
```

**Interview Tip:**
“I highlight that event delegation improves performance when handling many dynamic elements.”

---

### **54. Difference between ES5 and ES6 features?**

**Main ES6 Features:**

* `let`/`const`
* Arrow functions
* Classes
* Template literals
* Modules (`import/export`)
* Promises
* Spread/rest operators

**Example:**

```js
// ES5
var add = function(a, b) { return a + b; };

// ES6
const add = (a, b) => a + b;
```

**Interview Tip:**
“I mention ES6 made JS cleaner and closer to modern languages.”

---

### **55. What are higher-order functions in JavaScript?**

**Explanation:**

* Functions that take other functions as arguments or return functions.

**Example:**

```js
function higher(fn) {
  return function(x) { return fn(x) * 2; };
}
const double = higher(x => x + 1);
console.log(double(3)); // 8
```

**Interview Tip:**
“I say: map, filter, reduce are built-in higher-order functions.”

---

### **56. Difference between synchronous vs asynchronous execution?**

(Same as Q41 → emphasize blocking vs non-blocking.)

---

### **57. Difference between JSON and JavaScript objects?**

**Explanation:**

* JSON = string format for data exchange.
* JS object = in-memory data structure.

**Example:**

```js
let obj = { name: "John" };              // JS object
let json = JSON.stringify(obj);          // JSON
let parsed = JSON.parse(json);           // back to object
```

**Interview Tip:**
“I explain JSON is used for API data transfer, not for logic.”

---

### **58. Difference between map(), forEach(), filter(), and reduce()?**

* **map** → Returns new array (transform each element).
* **forEach** → Loops, no return.
* **filter** → Returns array with elements that pass condition.
* **reduce** → Accumulates to single value.

**Example:**

```js
let arr = [1,2,3];
console.log(arr.map(x => x*2));     // [2,4,6]
arr.forEach(x => console.log(x));  // prints 1,2,3
console.log(arr.filter(x => x>1)); // [2,3]
console.log(arr.reduce((a,b)=>a+b,0)); // 6
```

**Interview Tip:**
“I emphasize when to use each: map = transform, filter = select, reduce = summarize.”

---

### **59. Difference between mutable and immutable data in JS?**

* **Mutable:** Can change after creation (objects, arrays).
* **Immutable:** Cannot change (strings, numbers).

**Example:**

```js
let arr = [1,2];
arr.push(3); // mutated
let str = "hello";
str[0] = "H"; // no effect
```

**Interview Tip:**
“I explain immutability is important in React state management.”

---

### **60. Difference between functional programming and OOP in JS?**

* **FP:** Pure functions, immutability.
* **OOP:** Objects, classes, inheritance.

**Example:**

```js
// FP
const add = (a,b) => a+b;

// OOP
class Person { constructor(name) { this.name = name; } }
```

**Interview Tip:**
“I say JS supports both: React uses FP style, Node apps may use OOP.”

---

### **61. Difference between prototype and **proto**?**

* **prototype:** Property of functions (used when creating objects).
* ****proto**:** Property of objects that points to prototype.

**Example:**

```js
function Person() {}
Person.prototype.sayHi = () => console.log("Hi");

const p = new Person();
console.log(p.__proto__ === Person.prototype); // true
```

**Interview Tip:**
“I explain prototype is a blueprint, **proto** is a link.”

---

### **62. Difference between class and constructor function in JS?**

* **Constructor function:** Old way using functions.
* **Class:** ES6 syntax, sugar over prototype-based inheritance.

**Example:**

```js
// Constructor
function Person(name) { this.name = name; }

// Class
class PersonC { constructor(name) { this.name = name; } }
```

---

### **63. Difference between import and require?**

* **require:** CommonJS (Node.js, synchronous).
* **import:** ES6 modules, supports tree-shaking, async.

**Example:**

```js
// CommonJS
const fs = require("fs");

// ES6
import fs from "fs";
```

---

### **64. Difference between REST API and GraphQL in frontend usage?**

* **REST:** Multiple endpoints, fixed responses.
* **GraphQL:** Single endpoint, client asks for exactly what it needs.

**Example:**

```graphql
query {
  user(id: 1) { name, email }
}
```

**Interview Tip:**
“I say REST is simple & widely used, GraphQL is flexible and reduces over-fetching.”

---

### **65. Difference between debouncing and throttling in JavaScript?**

* **Debouncing:** Delay function execution until user stops triggering.
* **Throttling:** Ensures function executes at most once in given time.

**Example:**

```js
// Debounce
function debounce(fn, delay) {
  let timer;
  return function(...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

**Interview Tip:**
“I usually explain debounce is for search boxes, throttle is for scroll events.”

---


---

# **React.js Interview Questions (Q66–Q80)**

---

### **66. What is the difference between functional and class components?**

**Explanation:**

* **Class components**: ES6 classes, use `this`, lifecycle methods (`componentDidMount`).
* **Functional components**: Plain JS functions, use hooks (`useState`, `useEffect`).

**Example:**

```jsx
// Functional
function Greeting() {
  return <h1>Hello</h1>;
}

// Class
class GreetingC extends React.Component {
  render() {
    return <h1>Hello</h1>;
  }
}
```

**How to Answer in Interview:**
“I prefer functional components because they are simpler, use hooks instead of lifecycle methods, and improve performance compared to class components.”

---

### **67. What are React hooks? Common hooks?**

**Explanation:**
Hooks let you use state and lifecycle in functional components.

**Common Hooks:**

* `useState` → manage state
* `useEffect` → side effects
* `useContext` → consume context
* `useRef` → reference DOM elements
* `useMemo`, `useCallback` → optimization

**Example:**

```jsx
function Counter() {
  const [count, setCount] = React.useState(0);
  React.useEffect(() => console.log(count), [count]);
  return <button onClick={() => setCount(count+1)}>{count}</button>;
}
```

**How to Answer in Interview:**
“Hooks replaced many class component features. The most used hooks are useState and useEffect, but for optimization I use useMemo and useCallback.”

---

### **68. Difference between useEffect and useLayoutEffect?**

**Explanation:**

* **useEffect** → Runs after render is painted to screen (non-blocking).
* **useLayoutEffect** → Runs synchronously before painting (blocking).

**Example:**

```jsx
useEffect(() => { console.log("after paint"); });
useLayoutEffect(() => { console.log("before paint"); });
```

**How to Answer in Interview:**
“I use useEffect for most side effects like fetching data. I use useLayoutEffect only when I need to measure DOM elements before paint.”

---

### **69. What is the difference between controlled and uncontrolled components?**

**Explanation:**

* **Controlled**: React controls input via state.
* **Uncontrolled**: DOM manages its own state, accessed via `ref`.

**Example:**

```jsx
// Controlled
<input value={value} onChange={e => setValue(e.target.value)} />

// Uncontrolled
<input ref={inputRef} />
```

**How to Answer in Interview:**
“I prefer controlled components because they keep React state as the single source of truth. But uncontrolled is useful for quick forms.”

---

### **70. Difference between state and props in React?**

**Explanation:**

* **Props** → Passed from parent, read-only.
* **State** → Managed inside component, can change.

**Example:**

```jsx
function Child({name}) { return <h1>{name}</h1>; }
function Parent() {
  const [count, setCount] = React.useState(0);
  return <Child name="John" />;
}
```

**How to Answer in Interview:**
“I say props are for communication between components, state is for internal data that changes.”

---

### **71. Difference between useMemo and useCallback?**

**Explanation:**

* **useMemo** → Memoizes a computed value.
* **useCallback** → Memoizes a function reference.

**Example:**

```jsx
const value = useMemo(() => computeExpensive(x), [x]);
const memoFn = useCallback(() => doSomething(y), [y]);
```

**How to Answer in Interview:**
“I use useMemo for expensive calculations and useCallback to prevent unnecessary re-renders by memoizing functions.”

---

### **72. Difference between Context API and Redux?**

**Explanation:**

* **Context API** → Good for small apps, avoids prop drilling.
* **Redux** → State management library, scalable, middleware support.

**Example:**

```jsx
const ThemeContext = React.createContext();
```

**How to Answer in Interview:**
“I choose Context for small state sharing like theme or user data. For large-scale apps, Redux is better with middleware and debugging tools.”

---

### **73. What are React keys and why are they important?**

**Explanation:**

* Keys help React identify elements in lists to optimize rendering.

**Example:**

```jsx
{items.map(item => <li key={item.id}>{item.name}</li>)}
```

**How to Answer in Interview:**
“I always use unique IDs as keys to prevent re-rendering bugs. Using array index is a bad practice unless items never change.”

---

### **74. Difference between React.Fragment and a div wrapper?**

**Explanation:**

* **Fragment (`<>`)**: Group children without adding extra DOM node.
* **div**: Adds extra node, may break styling.

**Example:**

```jsx
<>
  <h1>Hello</h1>
  <p>World</p>
</>
```

**How to Answer in Interview:**
“I use Fragment when I don’t want unnecessary DOM nodes, which keeps the DOM cleaner.”

---

### **75. What is the difference between React virtual DOM and real DOM?**

**Explanation:**

* **Real DOM**: Browser’s actual UI representation, updates are expensive.
* **Virtual DOM**: Lightweight copy, React updates only changed parts.

**How to Answer in Interview:**
“I explain that React’s Virtual DOM improves performance by batching updates and minimizing real DOM manipulations.”

---

### **76. Difference between lazy loading and code splitting?**

**Explanation:**

* **Lazy loading** → Load components only when needed.
* **Code splitting** → Split bundle into smaller chunks for faster loading.

**Example:**

```jsx
const MyComponent = React.lazy(() => import("./MyComponent"));
```

**How to Answer in Interview:**
“I say code splitting is the technique, and lazy loading is one way of implementing it in React.”

---

### **77. Difference between React Router v5 and v6?**

**Main Changes in v6:**

* `<Switch>` replaced with `<Routes>`.
* Route element syntax changed (`element={<Comp />}`).
* Nested routes improved.

**Example:**

```jsx
// v5
<Route path="/home" component={Home} />

// v6
<Route path="/home" element={<Home />} />
```

**How to Answer in Interview:**
“I highlight that v6 simplifies routing with `element` prop and better nested routes.”

---

### **78. Difference between useState and useReducer hook?**

**Explanation:**

* **useState** → For simple state.
* **useReducer** → For complex state logic with multiple transitions.

**Example:**

```jsx
const [count, setCount] = useState(0);

const [state, dispatch] = useReducer((state, action) => {
  switch(action.type) {
    case "inc": return { count: state.count+1 };
    default: return state;
  }
}, { count: 0 });
```

**How to Answer in Interview:**
“I use useState for simple counters, and useReducer when I need structured state management like in forms.”

---

### **79. What is the difference between SSR and CSR in React?**

**Explanation:**

* **CSR (Client-Side Rendering):** Browser downloads JS, renders content on client.
* **SSR (Server-Side Rendering):** Server pre-renders HTML, sends to client.

**How to Answer in Interview:**
“I mention CSR is great for SPAs but slower initial load. SSR improves SEO and first paint speed — like in Next.js.”

---

### **80. Difference between hydration and rendering in React?**

**Explanation:**

* **Rendering**: React builds the DOM from scratch.
* **Hydration**: React attaches event listeners to already server-rendered HTML.

**How to Answer in Interview:**
“I explain hydration is specific to SSR — React takes over existing HTML and makes it interactive.”

---

# Performance, Security & Best Practices (Q81–Q90) — detailed answers + examples + exactly *how to say it in an interview*


---

### **81. How do you optimize frontend performance?**

**Explanation (practical checklist):**

* **Measure first:** use Lighthouse, WebPageTest, browser devtools to find real bottlenecks.
* **Reduce payloads:** minify & gzip/Brotli compress JS/CSS/HTML; tree-shake; remove unused code.
* **Code-splitting & lazy-loading:** split bundles so users download only needed code.
* **Optimize assets:** use modern image formats (WebP/AVIF), resize images, use `srcset`/`sizes`, lazy-load off-screen images.
* **Cache & CDN:** serve static assets from a CDN and use proper cache headers.
* **Reduce render-blocking resources:** defer or async scripts, inline critical CSS, load fonts smartly (`font-display: swap`).
* **Avoid layout thrashing:** batch DOM reads/writes, use transforms instead of top/left for animations.
* **Virtualize large lists:** render only visible rows (react-window, virtualization).
* **Optimize runtime:** memoize expensive renders (`useMemo`, `React.memo`), avoid unnecessary re-renders.
* **Use service workers:** for offline-first caching and fast repeat visits.
* **Set performance budgets** and monitor continuously.

**Examples:**

* Lazy image: `<img src="hero.jpg" loading="lazy" alt="...">`
* Preload script: `<link rel="preload" href="/static/chunk.js" as="script">`
* React code-splitting:

```jsx
const LazyComp = React.lazy(() => import('./BigComponent'));
```

**How to say it in interview (1–2 lines):**
“I start by measuring with Lighthouse/DevTools, then apply focused fixes — code-splitting and lazy-loading, compress and serve assets via CDN, inline critical CSS, optimize images and avoid unnecessary re-renders. I prefer measurable improvements and set performance budgets.”

---

### **82. Difference between *lazy loading* and *preloading*?**

**Explanation:**

* **Lazy loading:** *Delay* loading a resource until it’s needed (e.g., images below the fold or component when user navigates). Saves initial bandwidth.
* **Preloading:** *Tell the browser to fetch early* a resource you’ll need soon (but it does not execute it immediately). Helps reduce delay when resource is actually used.

**Examples:**

* Lazy image: `<img src="large.jpg" loading="lazy">`
* Preload a font:

```html
<link rel="preload" href="/fonts/foo.woff2" as="font" type="font/woff2" crossorigin>
```

* Prefetch (low priority for future nav): `<link rel="prefetch" href="/next-page.js">`

**How to say it in interview:**
“Lazy loading postpones work until needed; preloading fetches something early because you know you’ll need it soon. Use lazy for offscreen images/components and preload for critical assets like fonts or the next-route JS.”

---

### **83. What is *critical CSS* and why is it important?**

**Explanation:**

* **Critical CSS** = the minimal CSS required to render above-the-fold content on first load.
* Inlining that CSS in the HTML head speeds up the *first meaningful paint* because the browser can render UI without waiting for the full stylesheet. The rest of CSS can be loaded asynchronously.

**Example approach:**

```html
<head>
  <style>
    /* critical CSS: styles for header/hero that appear above-the-fold */
    .hero { display:flex; height:60vh; /* ... */ }
  </style>
  <link rel="stylesheet" href="styles.css" media="print" onload="this.media='all'">
</head>
```

(Or use a tool to extract critical CSS automatically during the build.)

**How to say it in interview:**
“Critical CSS is the small CSS needed to render above-the-fold content immediately; I inline it to speed first paint and load the rest asynchronously to improve perceived performance.”

---

### **84. Difference between HTTP/1.1, HTTP/2, and HTTP/3?**

**Explanation (concise):**

* **HTTP/1.1:** Text-based, single request per TCP connection (can reuse with keep-alive). Head-of-line blocking and many connections needed.
* **HTTP/2:** Binary protocol with **multiplexing** (many requests/responses over a single connection), header compression and server push (less needed nowadays). Reduces latency and makes many small resources efficient.
* **HTTP/3:** Uses **QUIC over UDP** (connection + transport improvements), faster connection establishment (reduced handshake), improved loss recovery and lower latency on poor networks.

**How to say it in interview:**
“HTTP/2 improves over 1.1 by multiplexing and compressing headers; HTTP/3 moves to QUIC/UDP for faster connection setup and better performance on lossy networks — overall fewer latency pitfalls.”

---

### **85. How to prevent XSS attacks in frontend?**

**Explanation (defense-in-depth):**

* **Avoid inserting unsanitized HTML**: prefer `textContent` / `innerText` over `innerHTML`.
* **Sanitize any HTML** coming from untrusted sources (e.g., use DOMPurify).
* **Escape user data** before rendering in templates.
* **Use Content Security Policy (CSP)** to restrict sources of scripts/styles and mitigate inline script execution.
* **HttpOnly cookies** for auth tokens (prevents JS access).
* **Avoid `eval()` and dynamic code execution.**
* **Validate and encode output** on server and client.

**Examples:**

* Safe text insertion:

```js
el.textContent = userInput; // safe
```

* Sanitizing HTML:

```js
const clean = DOMPurify.sanitize(dirtyHtml);
container.innerHTML = clean;
```

* Example CSP header:

```
Content-Security-Policy: default-src 'self'; script-src 'self' 'nonce-<random>';
```

**How to say it in interview:**
“I use a layered approach: never insert raw HTML, sanitize where needed (DOMPurify), set a strict CSP, and keep auth tokens HttpOnly. That combination prevents most XSS vectors.”

---

### **86. What is CORS and how does it work?**

**Explanation:**

* **CORS (Cross-Origin Resource Sharing)** controls whether a web page from one origin (scheme+host+port) can make requests to another origin. Browsers enforce the **same-origin policy** by default.
* When cross-origin requests are made, the browser checks server response headers like `Access-Control-Allow-Origin` to decide whether to allow the response. For non-simple requests (custom headers, methods like PUT), the browser performs a **preflight OPTIONS** request first.

**Example (server header):**

```http
Access-Control-Allow-Origin: https://myfrontend.com
Access-Control-Allow-Methods: GET, POST, OPTIONS
Access-Control-Allow-Headers: Content-Type
Access-Control-Allow-Credentials: true
```

**Node (Express) quick demo:**

```js
app.use((req, res, next) => {
  res.setHeader('Access-Control-Allow-Origin', 'https://myfrontend.com');
  res.setHeader('Access-Control-Allow-Credentials', 'true');
  next();
});
```

**How to say it in interview:**
“CORS is a browser security policy that blocks cross-origin requests unless the server opts in via specific response headers. For APIs, I configure proper `Access-Control-*` headers and handle preflight OPTIONS requests.”

---

### **87. Difference between `Cache-Control` and `Expires` header?**

**Explanation:**

* **Expires:** HTTP/1.0 header that provides a fixed date/time after which the resource is considered stale.
* **Cache-Control:** HTTP/1.1, more flexible and recommended — supports directives like `max-age`, `public`, `private`, `no-cache`, `must-revalidate`.
* Modern browsers prefer `Cache-Control` (and `max-age`) over `Expires` when both are present.

**Example:**

```
Cache-Control: public, max-age=31536000
Expires: Wed, 21 Oct 2026 07:28:00 GMT
```

**How to say it in interview:**
“Expires is the older date-based header; Cache-Control is newer and more flexible (use `max-age` etc.). I rely on `Cache-Control` for controlling caching behavior and set long max-age for immutable assets.”

---

### **88. What is a service worker and how does it help in PWA?**

**Explanation:**

* A **Service Worker** is a script that runs in the background (separate thread) and can intercept network requests, cache responses, enable offline use, background sync and push notifications. It acts like a programmable network proxy between the web app and the network. Essential for Progressive Web Apps (PWAs) to provide offline-first experiences and instant repeat loads.

**Basic example:**

```js
// register in page
if ('serviceWorker' in navigator) {
  navigator.serviceWorker.register('/sw.js');
}
```

```js
// sw.js (very simple)
self.addEventListener('install', evt => {
  // cache assets
});
self.addEventListener('fetch', evt => {
  evt.respondWith(caches.match(evt.request).then(r => r || fetch(evt.request)));
});
```

**How to say it in interview:**
“A service worker is a background script that can intercept requests and cache resources, enabling offline capability and very fast repeat loads — a core building block of PWAs.”

---

### **89. Difference between CSR, SSR, and SSG in frontend?**

**Explanation:**

* **CSR (Client-Side Rendering):** Browser downloads JS and renders UI on client (typical SPA). Pros: dynamic interactivity; Cons: slower first render and less SEO unless mitigated.
* **SSR (Server-Side Rendering):** Server renders HTML for each request and sends it to the client (faster first paint, better SEO). Examples: Next.js `getServerSideProps`.
* **SSG (Static Site Generation):** Pages are rendered at build time into static HTML (super-fast CDN delivery). Good for mostly static content. Examples: Next.js `getStaticProps`.

**How to say it in interview:**
“CSR is rendered in the browser (fast interactivity but slower initial paint), SSR pre-renders on the server for faster first paint and SEO, and SSG builds static HTML at compile time for maximum performance on static pages. I pick based on content dynamism and SEO needs.”

---

### **90. What are Web Components and why use them?**

**Explanation:**

* **Web Components** are a set of platform standards for building reusable, framework-agnostic UI components. Core parts:

  * **Custom Elements** (define new HTML tags)
  * **Shadow DOM** (encapsulated DOM & style scoping)
  * **HTML Templates** (template markup)
  * **ES Modules** (to export/import components)
* Benefits: encapsulation, reusability across frameworks, consistent API, style isolation.

**Example (basic custom element):**

```js
class MyButton extends HTMLElement {
  connectedCallback() {
    const s = this.attachShadow({mode: 'open'});
    s.innerHTML = `<style>button{padding:8px}</style><button>Click</button>`;
  }
}
customElements.define('my-button', MyButton);
```

Usage: `<my-button></my-button>`

**How to say it in interview:**
“Web Components let you create encapsulated, reusable custom HTML elements using Shadow DOM and Custom Elements — great for design-systems or sharing UI across different frameworks.”

---

---

## **General Frontend & Tools (Q91–Q100)**

---

### **91. What is the difference between Git merge and Git rebase?**

**Explanation:**

* **Merge:** Combines branches, keeps full history, adds a merge commit.
* **Rebase:** Moves your commits on top of another branch, cleaner history, no extra merge commit.

**Example (commands):**

```bash
# Merge
git checkout main
git merge feature-branch

# Rebase
git checkout feature-branch
git rebase main
```

**How to say in interview:**
“Merge preserves history with a merge commit, rebase rewrites history for a cleaner linear flow. I use rebase for feature branches, merge for integrating into main.”

---

### **92. Difference between package-lock.json and yarn.lock?**

**Explanation:**

* **package-lock.json**: Created by npm, locks dependencies.
* **yarn.lock**: Created by Yarn, same purpose.
  Both ensure consistent installs across environments.

**How to say in interview:**
“Both lock files guarantee identical dependency versions for everyone. `package-lock.json` is for npm, `yarn.lock` is for Yarn.”

---

### **93. Difference between npm and yarn?**

**Explanation:**

* **npm:** Default package manager with Node.js.
* **yarn:** Alternative from Facebook, focuses on speed, deterministic installs.
* Yarn v2+ works differently (Plug’n’Play), no node\_modules folder.

**Example:**

```bash
npm install react
yarn add react
```

**How to say in interview:**
“npm is the default package manager; Yarn introduced faster installs and lockfile improvements. Today, both are mature — I pick based on team standards.”

---

### **94. What is the difference between Webpack and Vite?**

**Explanation:**

* **Webpack:** Bundler, highly configurable, used for years.
* **Vite:** Next-gen build tool using native ES modules in dev (instant startup) + Rollup in prod.

**Example:**

```bash
# Create React app with Vite
npm create vite@latest my-app
```

**How to say in interview:**
“Webpack is powerful but slower for dev startup; Vite leverages ES modules for instant hot reloads, making it great for modern dev experience.”

---

### **95. Difference between monolith and microfrontend architecture?**

**Explanation:**

* **Monolith:** Entire frontend as one large codebase/deployment.
* **Microfrontend:** Split app into independent frontend modules owned by different teams.

**How to say in interview:**
“Monoliths are simple to manage initially but hard to scale with big teams. Microfrontends allow independent teams to ship features separately, but add complexity.”

---

### **96. What are Design Systems? Examples?**

**Explanation:**

* A **Design System** is a collection of reusable components, guidelines, and patterns for consistent UI/UX.
* Includes typography, colors, buttons, forms, etc.

**Examples:**

* Google **Material Design**
* IBM **Carbon**
* Microsoft **Fluent**

**How to say in interview:**
“A design system is a shared library of UI patterns/components that ensures consistency. For example, Material UI is a design system implementation.”

---

### **97. Difference between Tailwind CSS and traditional CSS frameworks?**

**Explanation:**

* **Tailwind:** Utility-first, highly customizable, small classes like `p-4`, `text-center`. Encourages composition.
* **Traditional (Bootstrap, Foundation):** Predefined components and grid system.

**Example:**

```html
<!-- Tailwind -->
<button class="bg-blue-500 text-white p-2 rounded">Click</button>

<!-- Bootstrap -->
<button class="btn btn-primary">Click</button>
```

**How to say in interview:**
“Bootstrap gives ready-made components; Tailwind gives atomic utility classes so I can build custom UIs without overriding styles.”

---

### **98. What are Lighthouse metrics for frontend performance?**

**Explanation:**
Google Lighthouse measures performance, accessibility, best practices, SEO, PWA.

**Key Metrics:**

* FCP (First Contentful Paint)
* LCP (Largest Contentful Paint)
* CLS (Cumulative Layout Shift)
* TTI (Time to Interactive)
* TBT (Total Blocking Time)

**How to say in interview:**
“I monitor Lighthouse metrics like LCP, CLS, and TTI. They measure how quickly and smoothly the page loads and becomes usable.”

---

### **99. Difference between responsive design and adaptive design?**

**Explanation:**

* **Responsive:** Fluid layout, adapts continuously to any screen size using flexible grids (%/vw).
* **Adaptive:** Predefined fixed layouts for specific breakpoints (320px, 768px, etc).

**Example:**

```css
/* Responsive */
.container { width: 80%; }

/* Adaptive */
@media (max-width: 768px) {
  .container { width: 700px; }
}
```

**How to say in interview:**
“Responsive design fluidly adapts to any screen, adaptive design switches between preset layouts at breakpoints.”

---

### **100. What are Progressive Web Apps (PWA)?**

**Explanation:**

* PWAs = Web apps with app-like features: offline support, installable, push notifications.
* Built with service workers + manifest.json.

**Example (manifest.json):**

```json
{
  "name": "My App",
  "start_url": "/",
  "display": "standalone",
  "icons": [{ "src": "icon.png", "sizes": "192x192", "type": "image/png" }]
}
```

**How to say in interview:**
“A PWA is a web app that feels like a native app — works offline, installable, push notifications. I use service workers + manifest to enable those features.”

---
