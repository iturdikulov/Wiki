---
date: 2026-01-06T10:21+03:00
tags:
  - blog
  - active
  - programming/vue
external:
  - https://vuejs.org/tutorial/
---

# Vue.js tutorial

Playground to to quickly give you an experience of what it feels like to work with Vue, right in the browser.

## Getting started

Vue use Single-File Component (SFC) for templates, reusable self-contained block of code that encapsulates HTML, CSS and JavaScript that belong together, written inside a `.vue` file.

The core feature of Vue is declarative rendering: with templates we can describe how the HTML should look based on JavaScript objects state. When the state changes, the HTML updates automatically.

When some state changed (objects) and it trigger updates, it's called a **reactive**.

We can declare reactive state using Vue's `reactive()` API. 

Objects created from `reactive()` are JavaScript [Proxies](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy) that work just like normal objects.

Example of proxy object:

```javascript
const target = {
    message1: "hello",
    message2: "everyone",
};

// Trap for getting property values
const handler2 = {
    // get() is an accessor property, it's called when the property is accessed
    get(target, prop, receiver) {
        return "world";
    },
};

const proxy2 = new Proxy(target, handler2);

console.log(proxy2.message1); // world
console.log(proxy2.message2); // world
```

### Using Vue Reactivity API

Vue `reactive()` function, only works on objects (including arrays and built-in types like `Map` and `Set`).

```javascript
reactive('test') // value cannot be made reactive
```

Counter example, if it used in template it will be updated automatically:

```javascript
import { reactive } from 'vue'

const counter = reactive({
    count: 0
})

console.log(counter.count) // 0
counter.count++

```
Vue `ref` function, works on any value type and create an object that exposes the inner value under a `.value` property:

```javascript
import { ref } from 'vue'

const message = ref('Hello World!')

console.log(message.value) // "Hello World!"
message.value = 'Changed'
```

### Templates

Reactive state declared in the component's `<script setup>` block can be used directly in the template:

```vue
<script setup>
import { ref, reactive } from 'vue'

const message = ref('Hello Man!')
const counter = reactive({
  count: 0
})
</script>

<template>
<h1>{{ message }}, value automatically unwrapped for more succint usage</h1>
<p>Count is: {{ counter.count }}</p>
<p>The content inside the mustaches is not limited to just identifiers or paths - we can use any valid JavaScript expression:</p>
<h1>{{ message.split('').reverse().join('') }}</h1>
</template>
```

---

What is a Single-File Component (SFC) in Vue?
<span class="f"></span>
A reusable, self-contained block of code (component) written in a `.vue` file that encapsulates HTML, CSS, and JavaScript that belong together. <!--SR:!2026-01-09,3,250-->

What is declarative rendering in Vue?
<span class="f"></span>
An approach where templates describe how the HTML should look based on JavaScript object state. The HTML updates automatically when the state changes. <!--SR:!2026-01-09,3,250-->

==Reactivity== - describes state (objects) that triggers automatic HTML updates when changed. <!--SR:!2026-01-09,3,250-->

What are the limitation of the `reactive()` function, how to bypass this limitation?
<span class="f"></span>
It only works on objects, including arrays and built-in types like Map and Set. It cannot make primitive values (like strings) reactive.
To bypass this, use the `ref()` function, which works on any value type and exposes the inner value under a `.value` property (in templates automatically unwrapped). <!--SR:!2026-01-09,3,250-->

Where is reactive state should be declared in Vue SFC to access them directly?
<span class="f"></span>
Inside the `<script setup>` block. <!--SR:!2026-01-09,3,250-->

What can be placed inside the double mustache `{{ }}` syntax in Vue templates?
<span class="f"></span>
Any valid JavaScript expression. <!--SR:!2026-01-09,3,250-->

