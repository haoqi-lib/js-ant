如何存储我们需要的信息呢？用变量！

## 变量是什么?

一个变量，就是一个用于存放数值的容器。这个数值可能是一个用于累加计算的数字，或者是一个句子中的字符串。变量的独特之处在于它存放的数值是可以改变的。让我们看一个简单的例子:

```html
<button>Press me</button>
```

```js
var button = document.querySelector('button')

button.onclick = function() {
  var name = prompt('What is your name?')
  alert('Hello ' + name + ', nice to see you!')
}
```

变量的另一个特性就是它们能够存储任何的东西 -- 不只是字符串和数字。变量可以存储更复杂的数据，甚至是函数。你将在后续的内容中体验到这些用法。

我们说，变量是用来存储数值的，那么有一个重要的概念需要区分。变量不是数值本身，它们仅仅是一个用于存储数值的容器。你可以把变量想象成一个个用来装东西的纸箱子。

![](https://raw.githubusercontent.com/haoqi-lib/js-ant/master/img/003-boxes.png)

## 声明变量

要想使用变量，你需要做的第一步就是创建它 -- 更准确的说，是声明一个变量。声明一个变量的语法是在 var 关键字之后加上这个变量的名字：

```js
var myName
var myAge
```

在这里我们声明了两个变量 myName 和 myAge。可以试着在自己的浏览器的控制台（console）中操作一下。

你可以通过使用变量的方式来验证这个变量的数值是否在执行环境中已经存在。例如，

```js
myName
myAge
```

以上这两个变量并没有数值，他们是空的容器。当你使用他们时，你会得到一个 undefined 的值。如果他们并不存在的话，那你就会得到一个报错信息。不信的话，可以尝试使用下面的变量，

```js
scoobyDoo
```

> 提示: 千万不要把两个概念弄混淆了，“一个变量存在，但是没有数值”和“一个变量并不存在” — 他们完全是两回事.

## 初始化变量

一旦你定义了一个变量，你就能够初始化它. 方法如下，在变量名之后跟上一个“=”，然后是数值:

```js
myName = 'Chris'
myAge = 37
```

现在回到控制台并且尝试输入这几行。每输入一条你都应该确认一下控制台输出的变量是不是你刚赋的值。 同样，你可以通过在控制台中输入变量的名称来返回该变量的值，执行：

```js
myName
myAge
```

也可以像这样，在声明变量的时候给变量初始化:

```js
var myName = 'Chris'
```

这可能是大多数时候你都会使用的方式， 因为它要比在单独的两行上做两次操作方便。

### 更新变量

变量赋值后，可以简单地给它一个不同的值来更新它。试试在控制台中输入下面几行:

```js
myName = 'Bob'
myAge = 40
```

## 变量命名的规则

你可以给变量赋任何你喜欢的名字，但有一些限制。 一般应当坚持使用拉丁字符(0-9,a-z,A-Z)和下划线字符。

* 不应当使用规则之外的其他字符，因为它们可能引发错误或者对国际用户来说难以理解。
* 变量名不要以下划线开头—— 以下划线开头的被某些 JavaScript 设计为特殊的含义，因此可能让人迷惑。
* 变量名不要以数字开头。这种行为是不被允许的，并且将引发一个错误。
* 一个可靠的命名约定叫做 "小写驼峰命名法"，用来将多个单词组在一起，小写整个命名的第一个字母然后大写剩下单词的首字符。我们已经在文章中使用了这种命名方法。
* 让变量名直观，它们描述了所包含的数据。不要只使用单一的字母/数字，或者长句。
* 变量名大小写敏感——因此 myage 与 myAge 是 2 个不同的变量。
* 最后也是最重要的一点—— 你应当避免使用 JavaScript 的保留字给变量命名。保留字，即是组成 JavaScript 的实际语法的单词！因此诸如 var, function, let 和 for 等，都不能被作为变量名使用。

> Note: 你能从[词汇语法—关键字](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords)找到一个相当完整的保留关键字列表来避免使用关键字当作变量。

好的命名示例:

```
age
myAge
init
initialColor
finalOutputValue
audio1
audio2
```

差的命名示例:

```
1
a
_12
myage
MYAGE
var
Document
skjfndskjfnbdskjfb
thisisareallylongstupidvariablenameman
```

## 变量类型

可以为变量设置不同的数据类型。

除了 null 和 undefined ，还有下面五种：

* Number

  你可以在变量中存储数字，不论这些数字是像 30（也叫整数）这样，或者像 2.456 这样的小数（也叫做浮点数）。与其他编程语言不同，在 JavaScript 中你不需要声明一个变量的类型。当你给一个变量数字赋值时，不需要用引号括起来。

  ```js
  var myAge = 17
  ```

* String

  字符串是文本的一部分。当你给一个变量赋值为字符串时，你需要用单引号或者双引号把值给包起来，否则 JavaScript 将会把这个字符串值理解成别的变量名。

  ```js
  var dolphinGoodbye = 'So long and thanks for all the fish'
  ```

* Boolean

  Boolean 的值有 2 种：true 或 false。它们通常被用于在适当的代码之后，测试条件是否成立。举个例子

  ```js
  var iAmAlive = true
  ```

* Array

  数组是一个单个对象，其中包含很多值，方括号括起来，并用逗号分隔。尝试在您的控制台输入以下行:

  ```js
  var myNameArray = ['Chris', 'Bob', 'Jim']
  var myNumberArray = [10, 15, 40]
  ```

  当数组被定义后，您可以使用如下所示的语法来访问各自的值，例如下行:

  ```js
  myNameArray[0] // should return 'Chris'
  myNumberArray[2] // should return 40
  ```

  此处的方括号包含一个索引值，该值指定要返回的值的位置。 您可能已经注意到，计算机从 0 开始计数，而不是像我们人类那样的 1。

* Object

  对象是现实生活中的事物的一种抽象模型。您可以有一个简单的对象，代表一个停车场，并包含有关其宽度和长度的信息，或者可以有一个代表一个人的对象，并包含有关他们的名字，身高，体重，他们说什么语言，如何说 你好，他们，等等。

  尝试在控制台输入以下行:

  ```js
  var dog = { name: 'Spot', breed: 'Dalmatian' }
  ```

  要检索存储在对象中的信息，可以使用以下语法:

  ```js
  dog.name
  ```

## 松散类型

JavaScript 是一种“松散类型语言”，不同于其他一些语言， JS 不需要指定变量将包含什么数据类型（例如 number 或 string）。

例如，如果你声明一个变量并给它一个带引号的值，浏览器就会知道它是一个字符串：

```js
var myString = 'Hello'
```

即使它包含数字，但它仍然是一个字符串，所以要小心：

```js
var myNumber = '500' // oops, this is still a string
typeof myNumber
myNumber = 500 // much better — now this is a number
typeof myNumber
```

尝试依次将上述代码输入您的控制台，看看结果是什么（无须输入//之后的注释）。 我们使用了一个名为 typeof()的特殊函数 ——它会返回所传递给它的变量的数据类型。 第一次在上面的代码中调用它，它应该返回 string，因为此时 myNumber 变量包含一个字符串'500'。 看看它第二次将返回什么。

## 参考

* https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables
