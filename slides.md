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

---

## My <strong class="text-blue-400">desired outcome</strong> for you

<div class="text-center invisible">Walk out of here with some fresh takes on <strong>what success looks like</strong> for a <strong>production-grade application.</strong></div>

---

## My <strong class="text-blue-400">desired outcome</strong> for you

<div class="text-center">Walk out of here with some fresh takes on <strong class="text-purple-400">what success looks like</strong> for a <strong class="text-blue-400">production-grade application.</strong></div>

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

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-2.png">

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-3.png">

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-4.png">

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-5.png">

---
transition: slide-left
level: 2
---

<img src="/imgs/fetch-6.png">

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

---

## 1. Handling of state

Managing data  <strong class="text-purple-400">throughout the application's lifecycle</strong>.

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

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

---

<img src="/imgs/state.png">

<span class="absolute bottom-12 left-12 text-2xl font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

---

## 2. Code volume

As the <strong class="text-purple-400">total amount of code grows</strong>,  <br/>so too does the difficulty of managing it.

<span class="absolute bottom-12 left-12 text-2xl  font-bold">The <span class="text-purple-400">iron triangle</span> of programming</span>

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

<img src="/imgs/math-formula.png" >

<span class="absolute bottom-12 left-12 text-2xl font-bold"><span class="text-purple-400">Domain, ranges</span> and testing</span>

---

## <strong class="text-purple-400">Domain</strong> in our <strong class="text-blue-400">input</strong><br/><strong class="text-purple-400">Range</strong> is what can be our <strong class="text-blue-400">output</strong>

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