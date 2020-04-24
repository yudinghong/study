# vue风格

## A必要的

\# 组件名为多个单词

```javascript 
// good example
Vue.component('todo-item', {
  // ...
})
```

\# 组件 `data` 必须是一个函数

\# `props` 尽可能详细

```javascript
// good example
props: {
  status: {
    type: String,
    required: true,
    validator: function (value) {
      return [
        'syncing',
        'synced',
        'version-conflict',
        'error'
      ].indexOf(value) !== -1
    }
  }
}
```

\# `v-for` 必须搭配 `key`

\# 避免 `v-for` 和 `v-if` 一起使用， 采用计算属性

\# 为组件样式设置作用域

\# `$_` 作为一个用户定义的私有属性的约定

\# 单文件组件的文件名应该要么始终是单词大写开头 (PascalCase)，要么始终是横线连接 (kebab-case)。

\# 应用特定样式和约定的基础组件 (也就是展示类的、无逻辑的或无状态的组件) 应该全部以一个特定的前缀开头，比如 Base、App 或 V。

>good examples
>>components/  
>>|- BaseButton.vue  
>>|- BaseTable.vue  
>>|- BaseIcon.vue
>
>>components/  
>>|- AppButton.vue  
>>|- AppTable.vue  
>>|- AppIcon.vue  
>
>>components/  
>>|- VButton.vue  
>>|- VTable.vue  
>>|- VIcon.vue

\# 单例组件名用`The`前缀

\# 和父组件紧密耦合的子组件应该以父组件名作为前缀命名
>good examples
>>components/  
>>|- TodoList/  
>>|- Item/   
>>&nbsp;&nbsp;|- index.vue  
>>&nbsp;&nbsp;|- Button.vue  
>>|- index.vue  

\# 组件名应该以高级别的 (通常是一般化描述的) 单词开头，以描述性的修饰词结尾。

\# 在单文件组件、字符串模板和 JSX 中没有内容的组件应该是自闭合的——但在 DOM 模板里永远不要这样做

