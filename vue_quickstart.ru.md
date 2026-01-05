---
date: 2026-01-05T10:13+03:00
tags:
    - blog
    - active
    - programming/vue
---

# Vue.js - Быстрый старт

Создаём boilerplate, команда установит и запустит create-vue — официальный инструмент для развёртывания проектов Vue. Также после запуска будут выводиться подсказки для возможности выбора ряда дополнительных функций, таких как TypeScript или поддержка тестирования:

```bash
pnpm create vue@latest
pnpm i && pnpm run dev
```

## Экземпляр приложения

Создание любого приложения Vue начинается с создания нового экземпляра приложения:

```javascript
import { createApp } from "vue";

const app = createApp({
    /* опции корневого компонента */
});
```

- Рекомендуемая конфигурация IDE — [Visual Studio Code](https://code.visualstudio.com/) + [Vue - Официальное расширение](https://marketplace.visualstudio.com/items?itemName=Vue.volar). Если используете другие редакторы, ознакомьтесь с разделом [поддержка IDE](https://ru.vuejs.org/guide/scaling-up/tooling.html#ide-support).
- Больше информации об инструментарии, включая интеграцию с бэкенд-фреймворками, обсуждается в разделе [Инструментарий](https://ru.vuejs.org/guide/scaling-up/tooling.html).
- Чтобы узнать больше об используемом инструменте сборки Vite, ознакомьтесь с [документацией Vite](https://vitejs.dev/).
- Если решили использовать TypeScript, ознакомьтесь с инструкцией по [использованию TypeScript](https://ru.vuejs.org/guide/typescript/overview.html).

## CDN

Если планируете использовать напрямую из CDN, ознакомьтесь с [документацией](https://ru.vuejs.org/guide/quick-start.html#using-vue-from-cdn).
Крайне аккуратно выбирайте CDN, проверяйте доступность из вашего региона.

Здесь использовали [unpkg](https://unpkg.com/), но также можно использовать любой другой CDN, который публикует npm-пакеты, например [jsdelivr](https://www.jsdelivr.com/package/npm/vue) или [cdnjs](https://cdnjs.com/libraries/vue). 

## Использование глобальной сборки

Пример Vue который загружает глобальную сборку Vue, где все API верхнего уровня доступны как свойства глобального объекта Vue:

```vue
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<div id="app"> {{ message }}</div>

<script>
// API верхнего уровня доступны как свойства глобального объекта Vue
// используем destruction для получения нужных нам функций
const { createApp, ref } = Vue

createApp({
setup() {
    const message = ref('Hello vue!')
    return {
        message
    }
}
}).mount('#app')
</script>
```

Многие примеры в руководстве по использованию Composition API будут использовать синтаксис `<script setup>`, который требует использования инструментов сборки. Если вы планируете использовать Composition API без этапа сборки, ознакомьтесь с использованием [опции `setup()`](https://ru.vuejs.org/api/composition-api-setup.html).

## Использование сборки в виде ES-модуля

Современный способ импорта используется синтаксис [ES-модулей](https://developer.mozilla.org/ru/docs/Web/JavaScript/Guide/Modules).

В большинство современных браузеров теперь встроенна поддержка ES-модулей, поэтому можно подключать Vue из CDN как нативный ES-модуль таким образом:

```vue
<div id="app">{{ message }}</div>

<!-- we use ES module script! -->
<script type="module">
  import { createApp, ref } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'

  createApp({
    setup() {
      const message = ref('Привет Vue!')
      return {
        message
      }
    }
  }).mount('#app')
</script>
```

## Использование Import maps

Для того чтобы использовать лаконичный импорт `import { createApp } from 'vue'`, нужно настроить `importmap` ([поддержка ограничена](https://caniuse.com/import-maps)):

```vue
<script type="importmap">
  {
    "imports": {
      "vue": "https://unpkg.com/vue@3/dist/vue.esm-browser.js"
    }
  }
</script>

<div id="app">{{ message }}</div>

<script type="module">
  import { createApp, ref } from 'vue'

  createApp({
    setup() {
      const message = ref('Привет Vue!')
      return {
        message
      }
    }
  }).mount('#app')
</script>
```

Также можно добавлять записи и для других зависимостей в import map — но убедитесь, что они указывают на версию ES-модуля библиотеки, которую собираетесь использовать.

## Разделение на модули

По мере углубления в руководство может понадобиться разделить код на отдельные файлы JavaScript, чтобы ими было легче управлять. Например:

```vue index.html
<div id="app"></div>

<script type="module">
  import { createApp } from 'vue'
  import MyComponent from './my-component.js'

  createApp(MyComponent).mount('#app')
</script>
```

```js my-component.js
import { ref } from 'vue'
export default {
  setup() {
    const count = ref(0)
    return { count }
  },
  template: `<div>Счётчик: {{ count }}</div>`
}
```

Если напрямую открыть `index.html` в браузере, то обнаружите, что он выдаёт ошибку, потому что ES-модули не могут работать по протоколу `file://` (из-за соображений безопасности). Чтобы исправить эту ситуацию, необходимо раздавать `index.html` по протоколу `http://` с помощью локального HTTP-сервера.

Для запуска локального HTTP-сервера для начала нужно установить Node.js, а затем запустить команду npx serve в том же каталоге, где находится HTML-файл. Можно использовать и любой другой HTTP-сервер, который умеет хостить статические файлы с правильными MIME-типами.

Как можно заметить, шаблон импортируемого компонента указан как строка JavaScript. При использовании VS Code можно установить расширение [es6-string-html](https://marketplace.visualstudio.com/items?itemName=Tobermory.es6-string-html) и добавить к этой строке префикс комментарием `/*html*/` чтобы получить подсветку синтаксиса в них.

---

С помощью какой команды рекомендуется создавать новый проект на Vue (boilerplate)?
<span class="f"></span>
`[p]npm create vue@latest` <!--SR:!2026-01-08,3,250-->

С чего начинается создание любого приложения Vue в коде (какой объект создаём)?
<span class="f"></span>
С создания экземпляра приложения с помощью функции `createApp` <!--SR:!2026-01-06,1,230-->

Для чего нужны import maps?
<span class="f"></span>
Чтобы использовать лаконичный синтаксис импорта (например, `import { ... } from 'vue'`). <!--SR:!2026-01-08,3,250-->

Из-за соображений безопасности. ES-модули работают только по протоколу ==http==. <!--SR:!2026-01-08,3,250-->

Как быстро запустить локальный HTTP-сервер для тестирования проекта без сложных инструментов сборки (Node.js)?
<span class="f"></span>
Выполнить команду `npx serve` в директории с проектом. <!--SR:!2026-01-08,3,250-->

При использовании Composition API напрямую через CDN (без этапа сборки) вы не сможете использовать синтаксис `<script setup>`. В этом случае необходимо использовать хук ==`setup()`==.
