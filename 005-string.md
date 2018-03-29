来注意力转向字符串——编程中调用的文本片段。我们将了解在 JavaScript 的常用字符串处理技巧，创建字符串、在字符串中转义引号、连接。

## 单引号和双引号

1.  在 JavaScript 中，您可以选择单引号或双引号来包装字符串。下面两种情况都可以:

```
var sgl = 'Single quotes.'
var dbl = "Double quotes"
sgl
dbl
```

2.  两者之间几乎没有什么区别，根据个人偏好来使用。但是，您应该选择一个并坚持使用它，不同的引用代码可能会让人混淆，特别是如果您在同一个字符串中使用不同的引号！

下面将返回一个错误:

```
var badQuotes = 'What on earth?"
```

3.  浏览器会认为字符串没有被关闭，因为在字符串中您没有使用其他类型的引号。例如，这两种情况都是可以的:

```
var sglDbl = 'Would you eat a "fish supper"?';
var dblSgl = "I'm feeling blue.";
sglDbl;
dblSgl;
```

4.  但是，不能在字符串中包含和最外层相同的引号。下面内容会导致错误，因为浏览器会搞不清楚到底字符串在哪里结束：

```
   var bigmouth = 'I've got no right to take my place...';
```

这个问题让我们很好地进入下一个主题。

## 转义（escape）字符串中的字符

要修复我们之前的问题代码行，我们需要对问题引号进行转义。转义意味着我们要让那些引号被当做文本而不是代码来对待。 JavaScript 中，通过在字符之前放一个反斜杠来实现转义。就像下面这样：

```
var bigmouth = 'I\'ve got no right to take my place...';
bigmouth;
```

## 连接字符串

可以使用加号来把字符串连接到一起。

```js
var one = 'Hello, '
var two = 'how are you?'
var joined = one + two
joined
```

joined 的结果是 `"Hello, how are you?"` 。

## 数字与字符

当我们尝试连接一个字符串和一个数字时，会发生什么?

尝试一下:

```js
'Front ' + 242
```

你可能会认为这会抛出一个错误，但它运行得很好。试图将把一个字符串看成一个数字并不是很讲的通，但是把数字作为一个字符串则不然，因此浏览器很聪明地将数字转换为字符串，并将这两个字符串连接在一起。

把一个数字组成的字符串穿换成真正的 number 型数据：

```js
var myString = '123'
var myNum = Number(myString)
typeof myNum
```

把一个数转换陈字符串

```js
var myNum = 123
var myString = myNum.toString()
typeof myString
```

## 参考

* https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Strings
