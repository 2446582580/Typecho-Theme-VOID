# Typecho Theme VOID

> 🐒 猴子打字机原理的产物

作为计算机术语时，VOID 的意思是「无类型」。

## 概览

![](https://raw.githubusercontent.com/AlanDecode/Typecho-Theme-VOID/master/screenshot.png)

## 特性

> 演示站点：[熊猫小A的博客](https://blog.imalan.cn)，介绍文章：[VOID：现在可以公开的情报](https://blog.imalan.cn/archives/247/)。

* PJAX
* 响应式设计
* 卡片式
* 代码高亮
* MathJax 公式
* 表情解析
* 图片排版
* 目录解析
* ...

总之用起来还算舒服。

## 开始使用

### 安装

**方法一：使用构建好的版本（推荐）**

1. 到 Release 页面下载构建包：[点击前往](https://github.com/AlanDecode/Typecho-Theme-VOID/releases)
2. 解压
3. **把解压后的文件夹重命名为 VOID**
4. 检查文件夹名是否为 VOID，不是的话改成 VOID
5. 检查文件夹名是否为 VOID，不是的话改成 VOID
6. 检查文件夹名是否为 VOID，不是的话改成 VOID
7. 上传文件夹至站点 /usr/themes 目录下
8. 后台启用主题

可选：将主题 `assets` 文件夹下的 `VOIDCacheRule.js` 复制一份到站点根目录，以启用 Service Worker 缓存。

**方法二：自己构建**

> 需要安装好 NodeJS

首先，clone 本仓库到本地：

```bash
git clone git@github.com:AlanDecode/Typecho-Theme-VOID.git ./VOID && cd ./VOID
```

然后安装依赖：

```bash
npm install -g gulp
npm install
```

最后构建打包：

```bash
gulp build
```

到此时，新鲜的主题就出现在了 build 文件夹下，把 build 文件夹上传到主题目录，重命名为 VOID，然后启用即可。本方法使你可以使用到最新的主题，但是它可能包含未知问题，适合愿意折腾的人。

### 添加归档页面

新建独立页面，自定义模板选择 `Archives`，内容留空。

### 添加友情链接

新建独立页面，然后如此书写：

```
<div class="board-list link-list">
[熊猫小A](https://www.imalan.cn)+(https://secure.gravatar.com/avatar/1741a6eef5c824899e347e4afcbaa75d?s=200&r=G&d=)
[熊猫小A的博客](https://blog.imalan.cn)+(https://secure.gravatar.com/avatar/1741a6eef5c824899e347e4afcbaa75d?s=64&r=G&d=)
</div>
```

在某些 Typecho 版本中，你需要使用 `!!!` 包裹以上代码，例如：

```
!!!
<div class="board-list link-list">
[熊猫小A](https://www.imalan.cn)+(https://secure.gravatar.com/avatar/1741a6eef5c824899e347e4afcbaa75d?s=200&r=G&d=)
[熊猫小A的博客](https://blog.imalan.cn)+(https://secure.gravatar.com/avatar/1741a6eef5c824899e347e4afcbaa75d?s=64&r=G&d=)
</div>
!!!
```

## 更新

同[开始使用](#开始使用)，区别是你可以直接覆盖主题文件，不禁用主题，这样你的主题设置就不会丢失。

## 开发

如果你要定制自己的版本，首先按照[安装](#安装)中的方法二装好环境。然后：

```bash
gulp dev
```

这会将依赖打包。你可以使用自己喜欢的方式编译 SCSS，或者使用：

```bash
gulp sass
```

监听 SCSS 更改然后实时编译。你可以添加自己想要的功能，满意后就提交代码。然后：

```bash
gulp build
```

构建你的主题。如果你对自己的更改很满意，**欢迎提出 Pull Request**。

## 鸣谢

### 开源项目

[JQuery](https://github.com/jquery/jquery) | [highlight.js](https://highlightjs.org/) | [MathJax](https://www.mathjax.org/) | [fancyBox](http://fancyapps.com/fancybox/3/) | [scrollTo](http://demos.flesler.com/jquery/scrollTo/) | [OwO](https://github.com/DIYgod/OwO) | [pjax](https://github.com/defunkt/jquery-pjax) | [yue.css](https://github.com/lepture/yue.css)

### 其他

[RAW](https://github.com/AlanDecode/Typecho-Theme-RAW) | [Mirages](https://get233.com/archives/mirages-intro.html) | [handsome](https://www.ihewro.com/archives/489/)

## License

MIT © [AlanDecode](https://github.com/AlanDecode)