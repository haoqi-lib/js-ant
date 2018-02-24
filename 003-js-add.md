可以通过不同的方式把 JS 添加到 html 页面中。

## 内部 JS

就是在 html 页面结束 </body> 标签前添加以下代码：

```html
<script>

  // JavaScript goes here

</script>
```

## 外部 JS

如果想要把我们的 JavaScript 放置在一个外部文件中，需要下面的步骤：

1. 首先，在跟你的简单 HTML 文件的同一目录下创建一个新的文件。命名为 script.js ——保证它以 .js 为文件扩展名，因为这是它被认作是 JavaScript 的方式。
2. 然后，把所有在你现在的 `<script>` 元素中的 js 提取出来并粘贴到 .js 文件。
3. 现在替换 `<script>` 元素为如下：

```js
<script src="script.js" />
```

4. 保存然后刷新你的浏览器。

## 内联 JS

这种形式是不推荐的。

```js
function createParagraph() {
  var para = document.createElement('p')
  para.textContent = 'You clicked the button!'
  document.body.appendChild(para)
}
```

```html
<button onclick="createParagraph()">Click me!</button>
```

这是一个用 JavaScript 来污染你的 HTML 的坏实践，而且它还不高效——你会需要在每个想要 JavaScript 应用到的按钮上包含 `onclick="createParagraph()"` 属性。

### 参考

从下面的链接有选择的拷贝内容进来，然后梳理了翻译不当的地方。

* https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/What_is_JavaScript
