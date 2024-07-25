---
# You can also start simply with 'default'
theme: eloc
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: Presentation on EffectTS 3.4+
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: none
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
---

<h1 class="bg-gradient-to-bl from-cyan-500 to-blue-500 bg-clip-text text-transparent leading-normal text-center">Production Grade<br/>Applications</h1>

...and how <strong class="text-blue-500">EffectTS</strong> helps to achieve this

<!-- ...Except I ran out of time for the EffectTS side of things -->

---

<h1 class="bg-gradient-to-bl from-cyan-500 to-blue-500 bg-clip-text text-transparent leading-normal text-center">Production Grade<br/>Applications</h1>

<del>...and how <strong class="text-blue-500">EffectTS</strong> helps to achieve this</del>

---
transition: slide-up
level: 2
---

# Table of <strong class="text-purple-400">contents</strong>

---

<ol>
  <li>
    <strong class="text-blue-400">Complexity</strong> and the <strong class="text-purple-400">iron triangle of programming</strong>
  </li>
  <li>
    <strong class="text-blue-400">Domains, ranges</strong> and <strong class="text-purple-400">testing</strong>
  </li>
  <li>
    <strong class="text-blue-400">Two types</strong> of <strong class="text-purple-400">errors</strong>
  </li>
  <li>
    <strong class="text-blue-400">Functional core,</strong> <strong class="text-purple-400">imperative shell</strong>
  </li>
  <li>
    <strong class="text-blue-400">Rolling forward</strong>
  </li>
</ol>

<!-- Except I also ran out of time for Rolling forward -->
---

<ol>
  <li>
    <strong class="text-blue-400">Complexity</strong> and the <strong class="text-purple-400">iron triangle of programming</strong>
  </li>
  <li>
    <strong class="text-blue-400">Domains, ranges</strong> and <strong class="text-purple-400">testing</strong>
  </li>
  <li>
    <strong class="text-blue-400">Two types</strong> of <strong class="text-purple-400">errors</strong>
  </li>
  <li>
    <strong class="text-blue-400">Functional core,</strong> <strong class="text-purple-400">imperative shell</strong>
  </li>
  <li>
    <del><strong class="text-blue-400">Rolling forward</strong></del>
  </li>
</ol>

---
transition: slide-up
level: 2
---

## What is <strong class="text-red-400">not on the list</strong>

<ol>
  <li>
    Not a primer on <strong class="text-red-400">functional programming</strong>
  </li>
  <li>
    Not a recap on
    <strong class="text-red-400">SOLID or GOF</strong>
  </li>
  <li>
    Not a push on <strong class="text-red-400">what we should do as a company</strong>
  </li>
</ol>

<!-- A lot of great content out there for SOLID and GOF. I wanted to explore some less-common ideas. -->

---

## My <strong class="text-blue-400">desired outcome</strong> for you

<div class="text-center invisible">Walk out of here with some fresh takes on <strong>what success looks like</strong> for a <strong>production-grade application.</strong></div>

---

## My <strong class="text-blue-400">desired outcome</strong> for you

<div class="text-center">Walk out of here with some fresh takes on <strong class="text-purple-400">what success looks like</strong> for a <strong class="text-blue-400">production-grade application.</strong></div>

<!-- A lot of this talk will be at an application level with some deviations here and there. In general, I hope everyone as a programmer can come out of this with fresh ideas or fresh arguments against these ideas. -->

--- 

# <strong class="bg-gradient-to-bl from-cyan-500 to-blue-500 bg-clip-text text-transparent leading-normal text-center">Complexity</strong>

<div class="text-center invisible">“We are not hardwired as humans to be able to comprehend the side-effects of complexity at scale.”</div>

---

# <strong class="bg-gradient-to-bl from-cyan-500 to-blue-500 bg-clip-text text-transparent leading-normal text-center">Complexity</strong>

<div class="text-center">“We are <strong class="text-blue-400">not hardwired as humans</strong> to be able to <strong class="text-blue-400">comprehend the side-effects</strong> of complexity at scale.”</div>


---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-1.png">

<!-- Ship it! There isn't even error handling. -->

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-2.png">

<!-- Next: Add validation -->

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-3.png">

<!-- Next: Add retries -->

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-4.png">

<!-- Next: Add interrupts -->

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-5.png">

<!-- Next: Add tracing -->

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-6.png">

<!-- What does less brain-load look like? -->

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-effect.png">

---
transition: slide-up
level: 2
---

<img src="/imgs/eap.png" class="p-20">

---
transition: slide-left
---

# The <strong class="text-purple-400">iron triangle</strong> of programming


---

<ol class="text-6xl">
  <li>
Handling of <strong class="text-red-400">state</strong>
  </li>
  <li>
    Code
    <strong class="text-red-400">volume</strong>
  </li>
  <li>
    Flow <strong class="text-red-400">control</strong>
  </li>
</ol>

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

<!-- We are going to walk through each of these, but this section isn't really a "problem/solution" part of the talk, but more of a "hey, these are some useful ideas to think about when talking complexity". -->

---

## 1. Handling of state

Managing data  <strong class="text-purple-400">throughout the application's lifecycle</strong>.

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

<!-- State management comes in many flavors and at very different layers, but let's walk through a contrived example of state management woes -->

---

<img src="/imgs/shared-state-1.png">

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

<img src="/imgs/shared-state-2.png">

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

<img src="/imgs/shared-state-3.png">

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

<img src="/imgs/shared-state-4.png">

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

<!-- In our example, we have two classes mutating shared state, and the purpose of our individual counter classes is lost. At scale, if we had an equivalent of 60 classes using this shared state, then that entanglement of shared state becomes problematic to debug as the application grows. -->

---

<img src="/imgs/state.png">

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

## 2. Code volume

As the <strong class="text-purple-400">total amount of code grows</strong>,  <br/>so too does the difficulty of managing it.

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

<!-- You look at something and think "there is a lot to take in". The old adage "the best code is zero code" -->

---

### Beyond code volume

<ol class="text-6xl">
  <li>
<strong class="text-red-400">Folder structure</strong>
  </li>
  <li>
    <strong class="text-red-400">Number of files</strong>
  </li>
  <li>
    <strong class="text-red-400">Code location</strong>
  </li>
</ol>

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

### Beyond a code repository

<ol class="text-6xl">
  <li>
<strong class="text-red-400">Number of repositories</strong>
  </li>
  <li>
    <strong class="text-red-400">Number of micro-services</strong>
  </li>
  <li>
    <strong class="text-red-400">Number of products</strong>
  </li>
</ol>

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

## Solutions to code volume?

<strong class="text-6xl invisible">Generate as much code as you practically can.</strong>

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>


---

## Solutions to code volume?

<strong class="text-6xl text-green-500">Generate as much code as you practically can.</strong>

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

## GitLab Walkthrough #1: Auto-generated micro-service client

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

<img src="/imgs/autogen-client.png" class="p-20">

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

## GitLab Walkthrough #2: Auto-generated mocks

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>
---

<img src="/imgs/autogen-mocks.png" class="p-20">

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---
transition: slide-up
level: 2
---

## 3. Control flow

The more brainpower required to <strong class="text-purple-400">understand, locate and<br/>follow it</strong>, the more difficult.

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>


---

<img src="/imgs/swift-contrived.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

<img src="/imgs/swift-5-5.png" >


<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

## Questions to ask

1. Do I understand this code (without brain melt)?
2. Do I understand the inputs and outputs?
3. Can I know the result of this code every single time?
4. Can I reuse this code? (If no, you need to understand the context as to why it exists.)
5. Can I test this code?


<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---
transition: slide-left
---

## <strong class="text-purple-400">Domain, ranges</strong> and testing

---

## <strong class="text-purple-400">Domain</strong> in our <strong class="text-blue-400">input</strong><br/><strong class="text-purple-400">Range</strong> is our <strong class="text-blue-400">output</strong>

---

<img src="/imgs/math-formula.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>



---

<img src="/imgs/math-discrete-graph.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/can-drink-1.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/can-drink-2.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/can-drink-3.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/card-family.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

## Pure function = no side effects

- Logging
- Changing state
- Writing files

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/add-1.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/add-2.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/add-with-side-effects.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

<img src="/imgs/add-without-side-effects.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---
transition: slide-left
---

# <strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong>

---

<ol class="text-6xl">
  <li>
    <strong class="text-red-400">Expected errors</strong>
  </li>
  <li>
    <strong class="text-red-400">Unexpected errors (defects)</strong>
  </li>
</ol>

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong></span>

---

<img src="/imgs/validation-1.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong></span>

---

<img src="/imgs/validation-2.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong></span>

---

<img src="/imgs/validation-3.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong></span>

<!-- What happens to the type signature when you throw errors? -->

---

<h2 class="font-6xl"><strong>Aim of the game:</strong> control what you <strong class="text-green-400">can</strong>, manage what you <strong class="text-red-400">can't</strong></h2>

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong></span>

---

<h2 class="font-6xl"><strong>Aim of the game:</strong> control as many <strong class="text-green-400">expected errors</strong> as you <strong class="text-green-400">can</strong>, manage <strong class="text-red-400">defects</strong> that you <strong class="text-red-400">can't</strong></h2>

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Two types</strong> of <strong class="text-red-400">errors</strong></span>

--- 

# <strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong>

--- 

<h2 class="font-6xl italic">An <span class="text-purple-400">architectural pattern</span> that combines <span class="text-green-400">functional programming principles</span> with <span class="text-blue-400">imperative programming</span>.</h2>

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

<!-- Multi-paradigm languages like Ruby, Python and JavaScript can benefit greatly from this. Other languages with opinions may not benefit so much. -->

--- 

<img src="/imgs/linkedin.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

--- 

<img src="/imgs/hanami.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

--- 

<img src="/imgs/dry-rb.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

---

#### Functional Core

- This is the inner part of your application where the main business logic resides.
- It consists of <strong class="text-green-400">pure functions that don't have side effects</strong>.
- These functions <strong class="text-green-400">always return the same output for a given input</strong>.
- They <strong class="text-green-400">don't modify global state or perform I/O operations</strong>.
- The functional core is easier to test, reason about, and maintain.

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

---

#### Imperative Shell

- This is the outer layer of your application that interacts with the outside world.
- It <strong class="text-blue-400">handles I/O operations, database calls, user interface, etc</strong>.
- It's <strong class="text-blue-400">where side effects are contained and managed.</strong>
- The imperative shell coordinates the flow of data between the outside world and the functional core.

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

---

<img src="/imgs/fcis-circle.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

--- 

<img src="/imgs/fcis-1.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

--- 

<img src="/imgs/fcis-2.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

--- 

<img src="/imgs/fcis-3.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

---

#### For us at AP+

- The imperative shell <strong>does not have to be the top-level of a function</strong>.
- That boundary is fluid, but likely somewhere between our <strong class="text-green-400">service layer</strong> and <strong class="text-purple-400">pure functions</strong>.

<span class="absolute bottom-12 left-12 text-2xl font-bold"><strong class="text-purple-400">Functional core,</strong><br/><strong class="text-blue-400">imperative shell</strong></span>

--- 

#### Conclusion

- How does the <strong class="text-blue-500">iron triangle of programming</strong> affects us?
- How does understanding <strong class="text-green-500">domain and range</strong> help us write better code?
- How could an approach with <strong class="text-purple-500">imperative shell, functional core</strong> make TypeScript <del>feel less shit</del> work for us?
- How should we manage our <strong class="text-red-500">expected vs unexpected errors</strong>?