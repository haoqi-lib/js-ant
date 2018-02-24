总结了 JS 数组最常用的各种操作。

## 创建数组

```js
var fruits = ['Apple', 'Banana']

console.log(fruits.length)
// 2
```

## 通过索引访问数组元素

```js
var first = fruits[0]
// Apple
var last = fruits[fruits.length - 1]
// Banana
```

## 遍历数组

```js
fruits.forEach(function(item, index, array) {
  console.log(item, index)
})
// Apple 0
// Banana 1
```

### 添加元素到数组的末尾

```js
var newLength = fruits.push('Orange')
// ["Apple", "Banana", "Orange"]
```

### 删除数组末尾的元素

```js
// remove Orange (from the end)
var last = fruits.pop()
// ["Apple", "Banana"];
```

### 删除数组最前面（头部）的元素

```js
// remove Apple from the front
var first = fruits.shift()
// ["Banana"];
```

### 添加元素到数组的头部

```js
// add to the front
var newLength = fruits.unshift('Strawberry')
// ["Strawberry", "Banana"];
```

### 找出某个元素在数组中的索引

```js
fruits.push('Mango')
// ["Strawberry", "Banana", "Mango"]

var index = fruits.indexOf('Banana')
// 1
```

### 通过索引删除某个元素

```js
// this is how to remove an item
var removedItem = fruits.splice(pos, 1)
// ["Strawberry", "Mango"]
```

### 从一个索引位置删除多个元素

```js
var vegetables = ['Cabbage', 'Turnip', 'Radish', 'Carrot']
console.log(vegetables)
// ["Cabbage", "Turnip", "Radish", "Carrot"]

var pos = 1,
  n = 2

var removedItems = vegetables.splice(pos, n)
// this is how to remove items, n defines the number of items to be removed,
// from that position(pos) onward to the end of array.

console.log(vegetables)
// ["Cabbage", "Carrot"] (the original array is changed)

console.log(removedItems)
// ["Turnip", "Radish"]
```

### 复制一个数组

```js
// this is how to make a copy
var shallowCopy = fruits.slice()
// ["Strawberry", "Mango"]
```

### 参考资料

MDN 上文档的转载

* https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array
