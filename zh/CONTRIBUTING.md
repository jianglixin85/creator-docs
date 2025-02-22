# 中文文档编写规范

格式规范的目的是为了提供统一的书写准则，并使成品文档有更好的阅读体验。

## 标题使用 #，与上下正文需要使用空行隔开

一级标题使用一个 #，二级标题使用两个 ##，以此类推。

一般情况下，不要跳级使用标题，例如一级标题下，不能直接出现三级标题。

## 关于产品名的写法

1. Cocos Creator
2. Cocos Creator 2.4.3
3. v2.4.3
4. v3.0
5. The engine (where refer to the runtime)
6. The editor (where refer to the IDE)

**版本**：

- 2.4.3 (3.0.0)
- 2.4.3 Preview (GA/RC/Alpha/Beta ...)
- 2.4.x (3.0.x)
- 2.4 (3.0)
- 2.x (3.x)

**不要使用以下写法**：

1. CCC or ccc
2. Cocos (where refer to Cocos Creator)
3. IDE (where refer to Cocos Creator)

## 专有英文名词、组件名使用正确的首字母大写

正确：

> 使用 GitHub 登录
>
> Sprite 组件

错误：

> 使用 github 登录
>
> sprite 组件

## 使用空格

### 中英文之间、中文与数字之间需要增加空格

正确：

> 本站点使用 Jekyll 搭建，应用 HPSTR 主题。文章保存在 `_posts` 目录下。
>
> 今天出去买菜花了 5000 元

错误：

> 本站点使用Jekyll搭建，应用HPSTR主题。文章保存在`_posts`目录下。
>
> 今天出去买菜花了5000元

完整的正确用法：

> 请尽量避免直接使用系统自带的 Ruby，推荐使用 rbenv 来管理本地 Ruby 运行环境，同时使用 ruby-build 来安装 Ruby，现在使用的 Ruby 版本为 2.1.1。

### 数字与单位之间需要增加空格

正确：

> 我家的带宽有 1 Gbps，硬盘一共有 10 TB。

错误：

> 我家的带宽有 1Gbps，硬盘一共有 10TB。

**例外：度／百分比与数字之間不需要增加空格**

正确：

> 今天是 233° 的高溫。
>
> 新 MacBook Pro 有 15% 的 CPU 性能提升。

错误：

> 今天是 233 ° 的高溫。
>
> 新 MacBook Pro 有 15 % 的 CPU 性能提升。

### 跳转链接和相邻的正文之间需要增加空格

跳转链接格式：**[跳转的文档名称]\(跳转的文档路径)**。使用半角（halfwidth）英文标点，且 [] 与 () 之间不要有空格

> e.g：[监听和发射事件]\(../scripting/events.md)。

正确用法：

> 详情请参考 [监听和发射事件](../scripting/events.md) 文档。

错误用法：

> 详情请参考[监听和发射事件](../scripting/events.md)文档。

### 添加跳转到 API 文档的跳转链接，两边需要加空格

跳转链接格式：**[跳转的文档名称]\(跳转的文档目录)**。使用半角（halfwidth）英文标点，且 [] 与 () 之间不要有空格

> e.g：[Mask API]\(\_\_APIDOC\_\_/zh/classes/Mask.html)。跨文档的文件名后缀要使用 **.html**

## 使用加粗且和相邻的正文之间加空格

**编辑器中的面板名称、组件或其他重要界面元素**，使用加粗表示，并且和相邻的正文之间需要加空格。

> 格式：打开 \*\*属性检查器\*\* 查看属性

正确：

> 打开 **属性检查器** 查看属性
>
> 点击 **创建** 按钮创建新节点
>
> 拖拽任意一张图片资源到 **Sprite Frame** 属性中

需要注意的是编辑器中的属性名，要按照属性检查器中显示的格式书写。

## 使用 backtick，且和相邻的正文之间加空格

### 脚本属性和方法名按照 API 中显示的格式书写，使用 backtick 表示，并且和相邻的正文之间加空格

> 格式：通过 \`this.node.scale\` 来设置节点的缩放

正确：

> 通过 `this.node.scale` 来设置节点的缩放
>
> `this.getComponent(cc.Sprite).spriteFrame` 可以动态改变节点渲染的图像

### 文件名和文件路径，使用 backtick 表示，并且和相邻的正文之间加空格

格式：\`/mypath/myfile.ts\`

如果是完整路径，前面需要加 /，如果不是完整路径则不需要

正确：

> 分包的目录在 `build/quickgame/dist` 目录下

## 使用空行

### 代码段落与上下文之间需要使用空行隔开

例如：

> 保存 Prefab，代码范例如下：<br>
>
> \```js<br>
> Editor.Ipc.sendToPanel('scene', 'scene:apply-prefab', node.uuid);<br>
> \```
>
> 继续正文部分。

效果如下：

> 保存 Prefab，代码范例如下：
>
> ```js
> Editor.Ipc.sendToPanel('scene', 'scene:apply-prefab', node.uuid);
> ```
>
> 继续正文部分。

### 图片与上下正文之间需要使用空行隔开

图片格式：**![图片说明]\(图片的相对路径)**。使用半角（halfwidth）英文标点，且 !、[]、() 三者之间不要有空格

> e.g：!\[background]\(quick-start/background.png)

如果图片是添加在正文中，那么和相邻的正文之间需要加空格

## 换行使用空行或者 \<br\>

如果使用回车键换行，在 GitBook 上没有换行效果并且会增加一个空格

**使用空行换行效果**：

> 第一行
>
> 第二行

**使用 \<br\> 换行效果**：

> 第一行<br>
> 第二行

**使用回车键换行效果（不推荐）**：

> 第一行
> 第二行

## 使用中英文标点符号

### 中文排版时，一律使用全角（fullwidth）中文标点

正确：

> 嗨！你知道吗？今天前台的小妹跟我说“喵”了哎！

错误：

> 嗨！你知道吗？今天前台的小妹跟我说"喵"了哎！
>
> 嗨！你知道吗?今天前台的小妹跟我说"喵"了哎!

### 中英排版时，一律使用全角（fullwidth）中文标点

正确：

> 核磁共振成像（NMRI）是什么原理都不知道？JFGI！

错误：

> 核磁共振成像(NMRI)是什么原理都不知道？JFGI！
>
> 核磁共振成像(NMRI)是什么原理都不知道?JFGI!

### 中英排版时，遇到完整的英文整句，整句内容使用半角（halfwidth）英文标点

正确：

> 乔帮主那句话怎么说的？“Stay hungry, stay foolish.”

错误：

> 乔帮主那句话怎么说的？“Stay hungry，stay foolish。”

## 使用顿号

**中文文档句子内部的并列词应该用全角顿号（、）分隔，而不用逗号，即使并列词是英语也是如此。**

正确：

> 科技公司有 Google、Facebook、腾讯、阿里和百度等。

错误：

> 科技公司有 Google, Facebook, 腾讯, 阿里和百度等。

**英文句子中，并列词语之间使用半角逗号（,）分隔**

> e.g.: Microsoft Office includes Word, Excel, PowerPoint, Outlook and other components.

**中文句子内部的并列词，最后一个尽量使用（和）来连接，使句子读起来更加连贯**

例如下面两个句子都可以，但第二个更优。

> 科技公司有 Google、Facebook、腾讯、阿里，以及百度等。
>
> 科技公司有 Google、Facebook、腾讯、阿里和百度等。

更多关于标点符号的使用请参考：<https://github.com/ruanyf/document-style-guide/blob/master/docs/marks.md>。

## 注意事项的书写格式

> 格式：> \*\*注意\*\*：中英文文档的中英文符号不要混用

当注意事项在两点以上时书写格式如下：

> \> \*\*注意\*\*：<br>
> \> 1. 第一点。<br>
> \> 2. 第二点。<br>
> \> 3. 最后一点。<br>

效果如下：

> **注意**：
> 1. 第一点。
> 2. 第二点。
> 3. 最后一点。

## 分点介绍

当正文使用 **-** 或者 **数字** 分点介绍时，分点中的正文包括图片都需要保留 4 个空格的缩进。

例如使用 **-** 分点介绍时：

> \- 分点介绍 1
>
> （4 个空格）开始第一个分点的正文部分。
>
> \- 分点介绍 2
>
> （4 个空格）开始第二个分点的正文部分。
>
> （4 个空格）!\[image]\(图片链接)

效果如下：

> - 分点介绍 1
>
>     开始第一个分点的正文部分。
>
> - 分点介绍 2
>
>     开始第二个分点的正文部分。
>
>     !\[image]\(图片链接)

例如使用 **数字** 分点介绍时：

> 1\. 分点介绍 1
>
> （4 个空格）开始第一个分点的正文部分。
>
> 2\. 分点介绍 2
>
> （4 个空格）开始第二个分点的正文部分。
>
> （4 个空格）!\[image]\(图片链接)

效果如下：

> 1. 分点介绍 1
>
>     开始第一个分点的正文部分。
>
> 2. 分点介绍 2
>
>     开始第二个分点的正文部分。
>
>     !\[image]\(图片链接)

## 表格统一使用左对齐

例如：

> | 属性    | 功能说明 |<br>
> | \:---- | :------ |<br>
> | 属性 1  | 说明 1  |<br>
> | 属性 2  | 说明 2  |

前后可保留适当的空格，方便编辑。

## 脚注写法

例如：

这是有脚注的内容。\[^1]

\[^1]: 这是脚注的注释内容。

效果如下：

这是有脚注的内容。[^1]

[^1]: 这是脚注的注释内容。

## 参考链接

- [中文文档格式规范](https://github.com/anjuke/coding-style/blob/master/text/chinese.md)
- [文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
- [中文技术文档的写作规范](https://github.com/ruanyf/document-style-guide)
