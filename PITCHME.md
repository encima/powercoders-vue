@snap[north span-99]
# VueJS
## Frontend: From the coders, for the coders
@snapend

@snap[south span-100 h1-white]
### [Chris Gwilliams](https://github.com/encima)
### Powercoders 4/11/2019
@snapend

---

@snap[north span-100]
# What is Vue?
@snapend

@snap[south span-100 h1-white]
@snapend

---

@snap[north span-99]
# What is Vue?
@snapend

@snap[south span-100 h1-white]
Vue is a `Frontend Framework`
@snapend


---

@snap[north span-99]
#### What is a Frontend Framework?!?
@snapend

@snap[south span-100 h1-white]
A frontend framework is a way to write a website without writing ALL of this:

```
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="mystyle.css">
  </head>
  <body>
    <h1></h1>
    <p></p>
    <script src="./index.js">
  </body>
</html>
```
PLUS: CSS AND JS AND MORE
@snapend

---


@snap[north span-100]
# That is great! What are the downsides?
@snapend

@snap[south span-100 h1-white]
@snapend


---

@snap[north span-100]
### That is great! What are the downsides?
@snapend

@snap[south span-100 h1-white]
* More to learn
* Some `magic`
* You cannot just 'serve' content
  * Harder SEO
  * Frontend becomes a lot like backend
@snapend


---

@snap[north span-100]
### So, how do we do it?
@snapend

@snap[south span-100 h1-white]
* Automatically
* With tools
* With docs!
@snapend


---

### Automatically

```
npm install -g vue-cli
mkdir powervue
cd powervue
vue-cli init webpack-simple
npm install
```

---

### With tools!

`npm run dev`

---

### With docs!

[Vue Org](vuejs.org)

---

### OK, but, why Vue?

![](https://miro.medium.com/max/1100/1*Q2t-jgIzVx_w1Cyy1YlbNw.png)

---

@snap[north span-100]
### Long Answer?
@snapend

@snap[south span-100 h1-white]
Vue is a community developed framework following the ECMAScript standard and implementable in JavaScript or TypeScript providing Single File Components and an agnostic build tooling, with easy to deploy support for cross platform development
@snapend

---

@snap[north span-100]
### Short Answer!
@snapend

@snap[south span-100 h1-white]
* Community developed
  * Not backed by Facebook (React), Google (Angular)
* Huge library of plugins and tools
* Supportive and large community
@snapend

---

### Show Me The Code!!!!

![](https://media.giphy.com/media/QHE5gWI0QjqF2/source.gif)

---

### `src/main.js`

```
import Vue from 'vue'
import App from './App.vue'

new Vue({
  el: '#app',
  render: h => h(App)
})
```

---

### `src/App.vue`

```
<template>
  <div id="app"> // What does this mean?
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      title: 'Vue for Powercoders!'
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Helvetica;
  text-align: center;
}
</style>
```

---


@snap[north span-100]
### Single File Components
@snapend

@snap[south span-100 h1-white]
* HTML, JS and CSS all in *1* file
* Combine HTML layout with JS logic
* Vue Templating
* CSS: Support for SASS/SCSS etc
* Lifecycle hooks

@snapend
---

### Running Your Site

`npm run dev`

WAIT!

---

### Changing the Code

Change the `title` variable to:

```
title: 'Power to the People!'
```

Save the file

Switch back to your browser

What happened?

---

### The Power of a Framework

* Hot Module Reloading
* JavaScript packages [Awesome-vue](https://github.com/vuejs/awesome-vue)
* Clean/Clear Code Structure that (with Vue) **YOU** decide!
* Reusable code
* Templating

---

@snap[north span-100]
### Getting Started
@snapend

@snap[south span-100 h1-white]

One file will not get you very far!

Vue lets you import other Vue files the same way as with JavaScript

`import Thing from thingsFile`

@snapend

---

@snap[north span-100]
### Getting Started: Components
@snapend

@snap[south span-100 h1-white]

* A component is a reusable HTML template with some Vue/JS logic
* Many components can make up one page (`view`)
* They allow you to break a page down into its smallest parts
* **What common component examples can you think of?**
@snapend

---

```
<template>
  <div id="app">
    <h1>{{title}}</h1>
    <intro-block></intro-block>
    <hr>
    <reg-form></reg-form>
  </div>
</template>

<script>
  import IntroBlock' from './components/intro-block'
  import RegForm' from './components/reg-form'

  export default {
    name: 'Powervue App',
    data() {
      return {
        title: 'Components! Components! Components!'
      }
    }
  }
</script>
```

---

### Reg Form

```
<template>
  <div id="reg-form">
    <input v-model="userInput" placeholder="Type Words Here!">
    <p>You typed: {{ userInput }}</p>
    <select v-model="selected">
      <option v-for="option in options" v-bind:value="option.value">
        {{option.text}}
      </option>
    </select>
    <p>You selected: {{ selected }}</p>
    <button v-on:click="handleClick">Click it real good!</button>
  </div>
</template>
```

---

### Reg Form: HTML and JS in Harmony

```
<script>

export default {
  name: 'RegForm',
  data() {
    return {
      userInput: undefined,
      selected: undefined,
      options: [
        {
          'text': '',
          'value': 'A'
        },
        {
          'text': '',
          'value': '2'
        },
        {
          'text': '',
          'value': 'iii'
        }
      ]
    }
  }
}
</script>
```

---

### Reg Form: Event Handling

```
...
data() {
  ...
},
methods: {
  handleClick() {
    alert('You really push my buttons')
  }
}
...
```

---

### Topics we have not covered!

* Vue modules (`router`, `vuex` etc)
* Build tools (`webpack`, `babel` etc)
* Amazing Vue libraries (`axios`, `quasar`, `vuetify`)

---

### Want More?

![](https://media1.giphy.com/media/co5nmPivPa42vv6IVm/200.webp?cid=790b7611fb3e7858cdd0aa33a5b83b7ae3f428d1ca566c91&rid=200.webp)

[Getting Started](https://vuejs.org/v2/guide/)

---

### How Can I Help?

* What more would you like to know?
* What was not explained well/rushed/unclear?
* What did you like?

[Email Me! chris@gwillia.ms](mailto:chris@gwillia.ms)

---

### Thanks!

![](https://media.giphy.com/media/yoJC2El7xJkYCadlWE/source.gif)

---


