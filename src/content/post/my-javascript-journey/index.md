---
title: "My JavaScript Journey"
description: "An exploration of my experiences and learnings in JavaScript."
publishDate: "2025-05-01"
tags: ["javascript", "history", "tech"]
---
I was poking around the `tsconfig.json` file, trying to make sense of all those mysterious properties, when I stumbled upon something that caught my eye — the `target` option.  
A long dropdown list appeared: `ES3`, `ES5`, `ES2015`, all the way to `ESNext`.  
At that moment, my knowledge of JavaScript's evolution was... let's say, *surface-level*.

Sure, I knew the basics:

* `var` was the old-school way, and `const`/`let` for closure sake.
    
* `async/await` was the superhero duo that saved us from the `then()` *\-callback hellstorm*.
    
* Arrow functions? Those were the cool upgrade to avoid messy `this` and `that` binding hacks.
    

Most of what I knew came from a scattered collection of blog posts, Twitter/X threads, and half-remembered advice from tech legends. Useful? Sure. Structured? **Not even close!**

## Why I'm Writing This

This post kicks off a new series where I basically go *back to school* — but on my own terms.  
I'm setting out to relearn (properly) the core concepts that have been floating half-formed in my head for years.  
The goal is to dig deep, connect the dots, and understand *why* JavaScript became what it is today.

Expect these articles to hit the sweet spot between \[ *Not too boring and academic* 😴, *Not too fluffy and shallow* 🌊\]. The idea is to build a strong mental model — one that's solid enough for me to explain things clearly (and hopefully help you level up too). And what better place to start than **the history of JavaScript itself**?  

In this inaugural installment of our series on the evolution of web development, we trace JavaScript’s journey from its humble beginnings as inline `<script>` tags to the sophisticated module and bundling ecosystems that power modern applications—and we glimpse where it may go next. We begin by exploring how JavaScript first enabled dynamic behavior in browsers, then examine how server-side and browser module standards (CommonJS, ES Modules) emerged, before diving into the bundler revolution (Browserify, Webpack, Rollup, esbuild). We conclude by surveying JavaScript’s native module support in browsers and runtimes (Node.js, Deno) and considering future directions such as edge-native modules, WebAssembly integration, and build-tool performance innovations.

## The Early Days: Script Tags and LiveScript

In May 1995, Brendan Eich of Netscape implemented a new embedded scripting language in just ten days, originally dubbed Mocha and then LiveScript, to inject dynamic behavior into static HTML pages ([1995: The Birth of JavaScript | Cybercultural - Web Development History](https://cybercultural.com/p/1995-the-birth-of-javascript/?utm_source=chatgpt.com)). By December 4, 1995, Netscape and Sun Microsystems officially announced “JavaScript,” marking its first public release alongside Navigator 2.0 ([Javascript announced 25 years ago today - Adafruit Industries](https://blog.adafruit.com/2020/12/04/javascript-announced-25-years-ago-today/?utm_source=chatgpt.com)). Early JavaScript lived entirely within `<script>` tags, executed sequentially by the browser’s parser without any module or packaging system ([JavaScript](https://en.wikipedia.org/wiki/JavaScript?utm_source=chatgpt.com)).

### Standardization with ECMAScript

One year later, in June 1997, JavaScript was standardized as ECMA-262 (ES1), formalizing the language’s core syntax and behavior, paving the way for cross-vendor compatibility ([JavaScript History - W3Schools](https://www.w3schools.com/js/js_history.asp?utm_source=chatgpt.com)).

## The Rise of Module Systems: CommonJS and Browserify

As JavaScript use expanded beyond the browser—particularly with the rise of Node.js—developers demanded a module system for code organization. In January 2009, the CommonJS working group formed (initially as “ServerJS”), defining a synchronous `require()` API for modules on both server and client ([Website:Index/history - CommonJS Spec Wiki](https://wiki.commonjs.org/wiki/Website%3AIndex/history?utm_source=chatgpt.com)). That same year, npm was launched (May 27, 2009), introducing a centralized package registry and installer for JavaScript libraries ([Node.js - Simple English Wikipedia, the free encyclopedia](https://simple.wikipedia.org/wiki/Npm?utm_source=chatgpt.com)).

To bridge CommonJS modules into browsers, developers created Browserify, whose first stable release arrived on June 9, 2011. Browserify traverses your `require()` calls and bundles all dependencies into a single script for the browser ([Browserify - Wikipedia](https://en.wikipedia.org/wiki/Browserify?utm_source=chatgpt.com)).

## The Bundler Boom: Webpack, Rollup, and Beyond

### Webpack: The Swiss Army Knife of Bundlers

In February 2014, Webpack debuted as a pluggable module bundler that not only handled JavaScript but could also process assets (CSS, images) via “loaders” and split code with “plugins” (e.g., code-splitting, hot module replacement) ([Webpack - Wikipedia](https://en.wikipedia.org/wiki/Webpack?utm_source=chatgpt.com)).

### Rollup: Tree-Shaking Pioneer

Rollup followed in May 2015 as a next-generation bundler focused on the ES Module format, offering pioneering tree-shaking to eliminate unused code and generate smaller library builds ([rollup 4.29.0-1 on npm - Libraries.io](https://libraries.io/npm/rollup?utm_source=chatgpt.com)).

### Modern Performance: esbuild

More recently, esbuild emerged in early 2020 as a Go-based bundler and minifier, claiming “10 to 100×” faster build times by leveraging parallelism and native binaries ([What is esbuild? - DEV Community](https://dev.to/zaydek/what-is-esbuild-2ofc?utm_source=chatgpt.com)) ([esbuild - Wikipedia](https://en.wikipedia.org/wiki/Esbuild?utm_source=chatgpt.com)).

## Native Modules: ES Modules in Browsers and Node

### In-Browser ES Modules

By 2017, major browsers shipped native support for `<script type="module">` (Chrome 61, Firefox 60, Safari 10.1, Edge 16), allowing developers to use `import`/`export` without bundlers ([ECMAScript modules in browsers - JakeArchibald.com](https://jakearchibald.com/2017/es-modules-in-browsers/?utm_source=chatgpt.com)).

### Node.js Embraces ESM

Node.js introduced experimental ESM support in v13.2.0 and stabilized it by v14.0.0—allowing `.mjs` files or `"type": "module"` in `package.json` to opt into native modules alongside traditional CommonJS ([Modules: ECMAScript modules | Node.js v23.11.0 Documentation](https://nodejs.org/api/esm.html?utm_source=chatgpt.com)).

### Enter Deno

In May 2020, Ryan Dahl unveiled Deno 1.0, a secure runtime built in Rust that natively supports TypeScript and ES Modules—reimagining server-side JavaScript with modern defaults (no `node_modules`, explicit permissions) ([Deno 1.0](https://deno.com/blog/v1?utm_source=chatgpt.com)).

## Looking Ahead: The Future of JavaScript

* **Edge-Native Modules & Serverless**: Browsers and runtimes will lean more heavily on standardized modules for function shipping to edge networks (Cloudflare Workers, Vercel Edge).
    
* **WebAssembly Integration**: WASM will complement JS modules for performance-critical tasks (graphics, cryptography), blurring lines between languages.
    
* **Zero-Config Tooling**: Emerging frameworks (Vite, Snowpack) and bundler-less builds will optimize developer experience with instant module resolution and hot reload.
    
* **Module Federation & Microfrontends**: Runtime module loading will enable independently deployed frontends to share code without global bundling.
    
* **AI-Augmented Coding**: Tools will leverage AI to auto-generate boilerplate, suggest optimizations, and even orchestrate module graphs.
    

---

## 10 Future Article Ideas

1. **“From Mocha to Modules: A Deep Dive into ECMAScript Standardization”**  
    Explore the evolution of TC39 proposals, Harmony, and ESNext features shaping JavaScript’s future.
    
2. **“Bundler Showdown: Webpack vs. Rollup vs. esbuild vs. Vite”**  
    Compare configurations, performance benchmarks, and ideal use cases for each major bundler.
    
3. **“Mastering Modern CSS: PostCSS, CSS Modules, and Module Federation”**  
    Examine how CSS workflows integrate with JS module bundlers for scalable styling.
    
4. **“TypeScript at Scale: Compiler Internals, Declaration Files, and Module Resolution”**  
    Unpack how TS handles type-safe modules across complex monorepos.
    
5. **“Serverless Edge with JavaScript: Building Functions for Cloudflare Workers and AWS Lambda”**  
    Show how ESM and WASM enable microservices on global edge networks.
    
6. **“Deno Deep Dive: Building Secure, TypeScript-First Applications”**  
    Guide readers through Deno’s permission model, std library, and Fresh framework.
    
7. **“WebAssembly + JavaScript: When and How to Leverage WASM in Your Apps”**  
    Walk through compiling Rust/C++ to WASM and integrating with JS module imports.
    
8. **“Automating Your Workflow: From npm Scripts to CI/CD with Module Bundlers”**  
    Teach best practices for linting, testing, and deploying frontends using modern build tools.
    
9. **“Module Federation in Practice: Architecting Microfrontends”**  
    Demonstrate runtime module loading across independently deployed teams.
    
10. **“AI in Code: Leveraging GPT-Powered Tools for JavaScript Refactoring and Productivity”**  
    Explore AI assistants, code generators, and their impact on developer workflows.
    

---

## Blog Name Suggestions

* **ModuleCraft** — Emphasizing mastery of JavaScript modules and tooling.
    
* **FrontForge** — A workshop-style brand for forging modern frontends.
    
* **ScriptRevolution** — Honoring JavaScript’s transformative history and future.
    
* **Bundler’s Almanac** — A play on “yearbook,” chronicling build tools and trends.
    
* **EdgeScript Insights** — Reflecting a focus on edge-native, performance-oriented JavaScript.