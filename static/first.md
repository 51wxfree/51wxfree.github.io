# 欢迎使用 CEditor Markdown 编辑器

**CEditor**是专注于微信公众号的编辑阅读器，利用CEditor可以使用 **Markdown** 语法编写微信公众号文章，编辑完后可以复制到公众号发布平台直接发布，真正的实现即看即所得：

* 更加贴合微信UI标准
* 支持实时预览
* 支持同步滚动
* 支持语法高亮
* 支持emoji表情

> CEditor解决了微信公众号编辑中遇见的一些编辑问题，增加了「工（ma）程（nong）师（men）」经常遇见的代码高亮、emoji问题。希望你会喜欢这种极（zhuang）客（bi）的体验

## 本编辑器支持快捷键
* `⌘+S` or `Ctrl+S`：保存编写的内容
* `⌘+Alt+U` or `Ctrl+Alt+U`：隐藏/显示顶部工具栏

## 什么是 Markdown
Markdown是一种方便记忆、书写的纯文本标记语言，用户可以使用这些标记符号以最小的输入代价生成极富表现力的文档：譬如您正在阅读的这份文档。它使用简单的符号标记不同的标题，分割不同的段落，**粗体** 、 *斜体* 、~~delete~~ 某些文字。["info" CEditor] 使用了 `showdown` 语法（一种markdown的扩展语法）

## 标题二
### 标题三
#### 标题四
##### 标题五，不常用
###### 标题六，不常用


## 1. 基本列表样式

* 偶是个无序列表
    - 我是个二级无序列表
* 真巧啊我也是个无序列表


1. 我是个有序列表啊
2. 嗯，me too~
3. markdown so easy! 妈妈再也不用担心我的**学习**了


## 2. 高亮一段代码

```js
// 新语法检测
import $ from 'jQuery'
$(document).on('click', ()=>{
  let that = this
  console.log(that)
})

var aceEditor = new ace.editor('#id')

$(function(){
  $('div').html('I am a div.');
});
```

上面是 `JavaScript`，下面是 `php`：

```php
echo 'hello,world'
```

## 支持emoji！

* Unicode支持：😈 💗 😄 🐂 👍
* github版本支持：:octocat: :cn: :red_car: :muscle: :smile: :sunglasses:

## 绘制表格
下面是个普通的表格
| 公众号 | id | 备注 |
|:-----|-----|:------:|


支持另外一种语法：
公众号        | id/网址       | 备注
------------ | ----------   | ------



## 扩展语法样式
此部分写法，会被转换为`span`包裹的文字，然后加上对应的样式属性

* ["success" 颜色扩展]
    * ["green" 内置绿色 green/success]
    * ["danger" 内置红色 danger/red]
    * ["blue" 蓝色 info/blue]
    * ["warning" 黄色 warning/yellow]
    * ["#ccc" 自定义颜色值#ccc] + ["#337ab7" 自定义颜色值#337ab7]
* 字号扩展
    - ["12px" 自定义字号12px]
    - ["120%" 自定义字号120%]
    - ["2em" 自定义字号2em]
* center和strong
    - ["center" 文字居中]
    - ["strong" 文字加粗]
* 任意自定义样式组合
    * ["padding-left:30px;blue;strong;center" 自定义css样式]

再一次感谢您花费时间阅读这份欢迎稿！

--eof--
