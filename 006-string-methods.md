通过字符串内置方法可以对字符串做什么有用的操作呢？查找文本字符串的长度，加入和分割字符串， 将字符串中的一个字符替换为另一个字符。

## 把字符串当做对象

我们重申一遍

> 在 javascript 中，一切东西都可以被当做对象。

例如创建一个字符串。

```js
var string = 'This is my string'
```

现在变量变成了一个字符串对象实例，所以可以有大量的属性和方法可以使用了。

### 查询字符串长度

使用 `length` 属性就可以做到。

```js
var browserType = 'mozilla'
browserType.length
```

返回值应该是 7。

### 获取特定字符

可以用方括号获取特定字符

```js
browserType[0]
browserType[browserType.length - 1]
```

## 在字符串中查找子字符串并提取它

查找一个字符串中是否包含一个子字符串

```js
browserType.indexOf('zilla')
```

返回 2 。因为子串“zilla”从“mozilla”内的位置 2（0，1，2 - 所以 3 个字符）开始。这样的代码可以用来过滤字符串。 例如，假设我们有一个 Web 地址列表，只想打印出包含“mozilla”的那些。

如果执行：

```js
browserType.indexOf('vanilla')
```

结果是 -1 ，因为没有找到该子符串。这个其实非常常用，例如

```js
if (browserType.indexOf('mozilla') !== -1) {
  // do stuff with the string
}
```

上面的  判断的意思是：如果 browserType 中不包含 mozilla 这个字符串的话。

当我们知道了子字符串的开始位置，就可以用 slice 来提取它

```js
browserType.slice(0, 3)
```

返回 `moz` 。

如果要得到特定位置之后的所有字符，就用

```js
browserType.slice(2)
```

结果是 `zilla` 。

## 改变大小写

```js
var radData = 'My NaMe Is MuD'
radData.toLowerCase()
radData.toUpperCase()
```

`toLowerCase` 全部改为小写，`toUpperCase` 改为大写。

## 更新字符串的一部分

```js
browserType.replace('moz', 'van')
```

## 参考

* https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Useful_string_methods
