# codedog

## 初衷

个人比较习惯用 markdown 记一些东西，有时候需要插入一些在线小 demo，最好还能在线编辑，用类似 [codepen](https://codepen.io/) 引入的话显得有些大材小用，便希望有一种方式，能在 markdown 中写 html，并且不会相互干扰，遂有此项目

我们可以比较下原始的 markdown 文件和用 codedog 二次生成后的文件：

- [原始的 markdown 文件](https://raw.githubusercontent.com/hanzichi/codedog/master/example/demo.md)／[效果](https://github.com/hanzichi/codedog/blob/master/example/demo.md)
- [codedog 二次生成后的 html 文件](https://github.com/hanzichi/codedog/blob/master/example/demo.html)／[效果](https://hanzichi.github.io/codedog/example/demo.html)

另外，这个项目是我为 [css-secrets](https://github.com/hanzichi/css-secrets) 特意创造的，更多应用可以点 [这里](https://github.com/hanzichi/css-secrets/blob/master/README.md) 查看

## 用法

因为纯属个人工具，没有很大的应用需求，故不再在 [npmjs](https://www.npmjs.com/package/codedog) 更新

该项目使用非常简单，支持模块引用和全局引用，个人推荐全局引用方式

### 本地安装

```bash
git clone git@github.com:hanzichi/codedog.git
npm install
npm link
```

### 应用

```bash
# local
node cli xx.md

# global
codedog xx.md

# advanced
codedog xx.md width height
```

没错，codedog 几乎不提供任何参数，唯二提供的两个可选参数是在线 demo 的宽度和高度：

- width (the width of the code editor as well as other code blocks, default to 100% of its parent node's width)
- height (the height of the code editor, default to `270` (px))

## 注意事项

- 该项目用于从 markdown 生成 html，并提供某些在线编辑／预览，如果没有这个需求，说明你不需要
- **markdown 中标注为 `html` 的代码块会被 codedog 解析**，并生成在线 demo，其余代码块不会解析
- 被解析的代码块，支持内联 css 和 js，支持绝对路径的外链 css 和 js
- 点击新页面打开，会在新的页面打开在线 demo

## lisence

MIT
