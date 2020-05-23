# 黑魔法 - Webstorm 智能跳转分享

已经记不清是第几次从尝试转其他编辑器失败，最终回到 Webstorm 的怀抱中来。Webstorm 智能的模板跳转真的让人欲罢不能，尤其是对于模板的跳转支持简直无人能敌。

虽然目前 VSCode 大火，但在模板和常用前端框架（如 Vue / Webpack) 的提示和支持上，仍然比不上 Webstorm。但或是因为收费问题，或是因为体积庞大、性能要求高，仍然有许多人没有深度使用过 Webstorm，体验过 Webstorm 智能分析和跳转带来的酸爽。这篇文章会通过搭建一个 Vue 的 Webpack 脚手架，带你体会 Webstorm 强大的一面。

## VSCode VS Webstorm

2020 年最当红的编辑器，非 VSCode 莫属。拥有微软的背书，同时坐拥上万插件，不论是编写哪一种语言，哪一个模板，都能在插件商店中找到解决方案。

作为一个低端前端切图仔，最常写的便是 Vue / Node.js 项目。就我目前的体验来说，VSCode + 对应官方插件所提供的功能仍然赶不上 Webstorm。个人给出的两款编辑器对比如下：

|名称|VSCode|Webstorm|
|----|----|----|
|语言框架支持情况| 非常好，支持多种语言，用途广泛 | 一般，只支持大前端开发常见语言和框架 |
|收费和支持情况| 免费，且前景亮眼，被大量植入为云 IDE| 国内 ￥65 / 月，苦逼学生党凭学生邮箱免费|
| 打开速度 | 极速，但安装太多插件会变慢，建议禁用不常用插件 | 冷启动很慢，并且打开后会建立索引，需要大量 CPU 资源|
| 内存占用 | 不多不少 | 多，尤其是依赖多、跳转多的情况|
|Git支持|一般，虽然有支持，但功能比较简陋，需配合 GitLens 使用| 强，checkout 分支时还会保存当前打开的窗口，此外还带有本地 History 功能 |
|CSS 提示| 弱，写在其他文件中的选择器得不到提示| 强，跨文件的选择器能够得到提示，@import 进来的选择器也能得到提示|
|Vue 模板跳转|一般，Vue `<scripts>` 内部可跳转，但 `<template>` 模板内无法跳转| 强，写在模板内的变量和方法都能够得到提示和跳转，命名重构时也能被统一改正|
|Webpack支持| 一般，不过安装了 webpack snippets 效率还行| 强，能够设置 webpack 配置文件，读取并分析得到编写、跳转提示，后面会详细介绍|
| 外部 link 的文件支持| 无 | 可在 url 点击 download，分析完成后可得到对应语法提示，后续会有详细介绍|
| Node 支持| 强，如果纯写 JS，跳转和提示基本无忧 | 强，同 VSCode |
| Typescript 支持| 强，亲生儿子 | 强，同 VSCode |
| 插件情况 | 极多，但不少过时和质量差的插件也在其中，插件需自行体验 | 少，但主要功能均已集成 |
| markdown 支持| 非常好，美观且性能高 | 极差，样式丑且性能极差，滚动跟随也有问题 |
| npm 支持 | 一般，可以检测 npm scripts | 强，常用字段能得到提示且有解释，编写 npm scripts 会有 bash 命令和路径提示|

上面的对比纯个人主观感受，如有纰漏或更好解决方案，欢迎评论指出。

## 如何食用

我将搭建一个 Vue 的 Webpack 脚手架，并在搭建过程中带你领略 Webstorm 的各种便利之处。你也可以同时使用 Webstorm 和 VSCode 同时搭建，来横向对比两款编辑器更适合你。

文章涉及 Vue 和 Webpack 知识，需要你具有其基础知识，并有一定的开发经验。

## Enjoy ✌️

让我们开始吧！

```bash
# 克隆项目
git clone git@github.com:wizzeng/webstorm_dev_share.git
```

## 章节

- [1 - Webstorm 下的 Webpack 配置提示 & 外部资源跳转](create_project.md)