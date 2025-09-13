# Frontend_QNA



---

# 📌 Frontend Interview One-Line Cheat Sheet (100 Qs)

### **HTML (1–15)**

1. Semantic tags = meaningful (`<header>`, `<article>`).
2. Block = full width, Inline = content width, Inline-block = inline + can size.
3. `<div>` = block container, `<span>` = inline container.
4. HTML5: semantic tags, audio/video, canvas, storage APIs, new inputs.
5. HTML = forgiving, XHTML = strict XML rules.
6. `id` = unique, `class` = reusable.
7. Relative = based on file, Absolute = full URL, Root = from site root.
8. `data-*` = store custom data for JS.
9. `<script>` blocks, `async` loads & runs ASAP, `defer` runs after parse.
10. `<link>` loads faster, `@import` slower.
11. Meta tags = metadata (charset, SEO, viewport).
12. Canvas = bitmap, SVG = vector.
13. localStorage = permanent, sessionStorage = tab session, cookies = sent with requests.
14. ARIA attributes = accessibility for screen readers.
15. `<section>` thematic, `<article>` self-contained, `<aside>` side info, `<main>` core content.

---

### **CSS (16–35)**

16. Relative = shift from self, Absolute = ancestor, Fixed = viewport, Sticky = scroll sticks.
17. Inline = `style=""`, Internal = `<style>`, External = `.css` file.
18. `%` = parent, `em` = parent font, `rem` = root font, `vw/vh` = viewport.
19. Same as 16.
20. Flexbox = 1D, Grid = 2D layouts.
21. Inline = can’t size fully, Block = full control.
22. z-index = stacking order, only on positioned elements.
23. (Repeat of 16 with examples).
24. Specificity = Inline > ID > Class > Element.
25. `visibility:hidden` keeps space, `display:none` removes.
26. Transform = change shape, Transition = smooth change, Animation = keyframes.
27. Inline CSS = high priority, External = better performance (cached).
28. Pseudo-class = state (`:hover`), Pseudo-element = part (`::before`).
29. `px` absolute, `em/rem/%` relative.
30. Media queries = style by screen size.
31. min-width = mobile-first, max-width = desktop-first.
32. Flexbox = alignment, Grid = layout.
33. Relative path = based on file, Absolute = root or full URL.
34. React inline style = object, class = className.
35. BEM = block\_\_element--modifier naming avoids conflicts.

---

### **JavaScript (36–65)**

36. var = function-scoped, let = block-scoped, const = block-scoped no reassign.
37. `==` loose (coerces), `===` strict.
38. Hoisting = declarations move to top.
39. null = intentional empty, undefined = not assigned.
40. Closure = inner fn remembers outer vars.
41. Sync = blocks, Async = non-blocking.
42. Bubbling = child→parent, Capturing = parent→child.
43. call = args list, apply = args array, bind = returns bound fn.
44. Shallow copy = refs inside shared, Deep copy = full independent.
45. Promise = future value (pending/fulfilled/rejected).
46. Chaining = `.then`, async/await = cleaner syntax.
47. localStorage = persistent, sessionStorage = tab life.
48. setTimeout = once, setInterval = repeat.
49. Arrow fn = no `this`, normal fn = dynamic `this`.
50. for..in = keys, for..of = values.
51. DOM = page structure, BOM = browser APIs.
52. innerHTML = HTML, innerText = text only.
53. Delegation = attach to parent, Handling = direct.
54. ES6 adds let/const, classes, arrow fn, modules, promises.
55. Higher-order fn = takes/returns fn (map/filter/reduce).
56. Sync blocks, Async doesn’t.
57. JSON = string, JS object = runtime.
58. map = transform, forEach = iterate, filter = select, reduce = accumulate.
59. Mutable = can change (obj/array), Immutable = can’t (string/number).
60. FP = pure functions, OOP = classes/objects.
61. prototype = fn blueprint, **proto** = object link.
62. Class = ES6 syntax, Constructor fn = old way.
63. require = CommonJS, import = ES6 modules.
64. REST = multiple endpoints, GraphQL = one endpoint flexible queries.
65. Debounce = wait till stop, Throttle = limit rate.

---

### **React.js (66–80)**

66. Functional = hooks, Class = lifecycle & `this`.
67. Hooks = state/lifecycle in functions (useState, useEffect).
68. useEffect = after paint, useLayoutEffect = before paint.
69. Controlled = React state controls input, Uncontrolled = DOM manages.
70. Props = external read-only, State = internal mutable.
71. useMemo = memoize value, useCallback = memoize fn.
72. Context = small apps, Redux = large scalable apps.
73. Keys = unique IDs to optimize list rendering.
74. Fragment = no extra DOM node, div adds node.
75. Virtual DOM = lightweight copy, Real DOM = browser actual.
76. Lazy loading = load when needed, Code splitting = break bundles.
77. Router v6 = `<Routes>` + `element` prop, simpler nested routes.
78. useState = simple state, useReducer = complex logic.
79. CSR = client renders, SSR = server renders, SEO friendly.
80. Rendering = build DOM, Hydration = attach events to SSR HTML.

---

### **Performance, Security & Best Practices (81–90)**

81. Optimize: code-split, lazy-load, CDN, cache, optimize images, reduce re-renders.
82. Lazy load = delay, Preload = fetch early.
83. Critical CSS = above-the-fold CSS inline for fast paint.
84. HTTP/1.1 = sequential, HTTP/2 = multiplexing, HTTP/3 = QUIC/UDP.
85. Prevent XSS: escape, sanitize, CSP, avoid eval.
86. CORS = server tells browser which origins allowed.
87. Cache-Control = flexible modern, Expires = older fixed date.
88. Service Worker = background script, offline cache, PWA.
89. CSR = SPA in client, SSR = pre-render per request, SSG = prebuilt static.
90. Web Components = custom elements + Shadow DOM, reusable.

---

### **General Frontend & Tools (91–100)**

91. Merge = preserves history, Rebase = linear history.
92. package-lock = npm lock file, yarn.lock = yarn lock file.
93. npm = default manager, Yarn = faster alt.
94. Webpack = older, heavy, Vite = fast dev + Rollup prod.
95. Monolith = single app, Microfrontend = split apps per team.
96. Design System = reusable UI components + guidelines (Material, Carbon).
97. Tailwind = utility classes, Bootstrap = pre-built components.
98. Lighthouse metrics = FCP, LCP, CLS, TTI, TBT.
99. Responsive = fluid, Adaptive = fixed breakpoints.
100. PWA = web app with offline/installable features.

---


