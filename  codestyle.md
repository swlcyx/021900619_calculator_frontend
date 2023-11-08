# 前端代码风格

本指南在规范 Vue 3 前端项目的代码风格，以提高代码的可读性、可维护性和一致性。请在项目中遵循以下准则。

## 目录

1. [命名规范](https://chat.aichatos.top/#命名规范)
2. [组件规范](https://chat.aichatos.top/#组件规范)
3. [代码格式化](https://chat.aichatos.top/#代码格式化)
4. [注释规范](https://chat.aichatos.top/#注释规范)
5. [其他规范](https://chat.aichatos.top/#其他规范)

## 命名规范

- 使用驼峰命名法（camelCase）命名变量、函数和方法。
- 使用 PascalCase 命名组件和类。
- 使用全大写的 SNAKE_CASE 命名常量。
- 避免使用单个字符命名，除非用于计数器或临时变量。

```js
javascriptCopy Code// 示例
const firstName = 'John';
function getUserInfo() { /* ... */ }
export default class MyComponent { /* ... */ }
const MAX_COUNT = 10;
```

## 组件规范

- 组件名应该具有描述性，使用单词或短语来表示组件的功能。
- 组件文件名应该与组件名保持一致，并且使用 PascalCase 命名。

```js
javascriptCopy Code// 示例
// MyComponent.vue
export default {
  name: 'MyComponent',
  // ...
}
```

- 组件选项的顺序应该按照以下顺序排列：
  - `name`
  - `components`
  - `props`
  - `data` (如果使用对象语法)
  - `computed`
  - `watch`
  - `methods`
  - `lifecycle hooks`

```js
javascriptCopy Code// 示例
export default {
  name: 'MyComponent',
  components: { /* ... */ },
  props: { /* ... */ },
  data() { /* ... */ },
  computed: { /* ... */ },
  watch: { /* ... */ },
  methods: { /* ... */ },
  created() { /* ... */ },
  mounted() { /* ... */ },
  // ...
}
```

## 代码格式化

- 使用 2 个空格作为缩进。
- 在每个代码块（如函数、循环、条件语句）之间使用空行进行分隔，以提高可读性。
- 在逗号后面添加一个空格，但在冒号前面不添加空格。

```js
javascriptCopy Code// 示例
function myFunction() {
  const array = [1, 2, 3];
  
  for (let i = 0; i < array.length; i++) {
    // ...
  }
  
  if (condition) {
    // ...
  } else {
    // ...
  }
  
  const obj = {
    key1: value1,
    key2: value2,
  };
  
  // ...
}
```

## 注释规范

- 使用单行注释 (`//`) 或多行注释 (`/* ... */`) 来解释代码的意图和功能。
- 在复杂的代码块或算法旁边添加注释，以提高可读性。
- 避免使用无意义或废弃的注释。

```js
javascriptCopy Code// 示例
// 计算两个数字的和
function add(a, b) {
  return a + b;
}

/*
  复杂算法示例：
  1. ...
  2. ...
  3. ...
*/
function complexAlgorithm() {
  // ...
}
```

## 其他规范

- 尽量避免使用 `!important`，除非在必要情况下才使用。
- 使用单引号 (`'`) 包裹字符串，除非字符串内部包含了单引号。
- 使用双引号 (`"`) 包裹 HTML 属性值。
- 在组件模板中，使用 kebab-case 命名属性和事件。

```js
htmlCopy Code<!-- 示例 -->
<template>
  <div :class="myClass" @click="handleClick"></div>
</template>

<script>
export default {
  data() {
    return {
      myClass: 'my-class',
    };
  },
  methods: {
    handleClick() {
      // ...
    },
  },
};
</script>
```

