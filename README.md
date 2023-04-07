# OOCSS

简单易用的组合式css库

实际开发过程中，总是会有大量简单而又不可或缺的css被反复添加。

OOCSS没有任何依赖，OOCSS包含了开发过程中最常用到的样式，通过类名组合的方式，避免了重复声明, 使我们不用离开html代码就可以完成样式设定

[![NPM version][npm-image]][npm-url]

[npm-image]: https://img.shields.io/badge/npm-v0.0.9-blue.svg
[npm-url]: https://www.npmjs.com/package/oocss

简体中文 | [English](./README-en.md)

## installation

```
$ npm install oocss
```

## Usage

```javascript
import 'oocss'
// or 
import 'oocss/src/index.css'

<div class="mgt-l pd-m tc-10 ta-c "></div>
```

```css
/** 统一使用变量，在保持一致性的同时，修改起来也极为方便 */
:root {
  --primary-color: #1890ff;
  --success-color: #52c41a;
  --warning-color: #faad14;
  --error-color: #f5222d;
  --gray-1: #ffffff;
  --gray-2: #fafafa;
  --gray-3: #f5f5f5;
  --gray-4: #e8e8e8;
  --gray-5: #d9d9d9;
  --gray-6: #bfbfbf;
  --gray-7: #8c8c8c;
  --gray-8: #595959;
  --gray-9: #262626;
  --gray-10: #000000;
  --size-s: 8px;
  --size-m: 16px;
  --size-l: 24px;
}
```

### 命名规则

缩写-值-伪类  
__尺寸__ 0： 0px，s: size-s, m: size-m, l: size-l  
__颜色__ 1-10，gray-1 ~ gray-10, p: primary-color, s: success-color, w: warning-color, e: error-color  

缩写通常只有2个字符，一个类通常也只包含一个样式  
.mg-l { margin: var(--size-l); }  
.dp-f { display: flex; }  
.ta-c { text-align: center; }

除了top, bottom, left, right这4个样式没有缩写，缩写目前最多3个字符，相当简洁  
.bgc-p { background-color: var(--primary-color); }  
.mgt-s { margin-top: var(--size-s); }  
.bdb { border-bottom: 1px solid var(--gray-5); }
.bdc-3 { border-color: var(--gray-3); }  

### demo
文字居中，灰色，鼠标悬停主题色，加粗，下划线，内边距小，上下外边距大，灰白背景，边框，阴影，鼠标点击样式
``` html
<div class="ta-c tc-7 tc-p-h fw-b td-u pd-s mgv-l bgc-2 bd bsd-5 cs-p">Hello oocss<div>
```
flex等分水平垂直居中，dp-f1在设置display: flex的同时会给所有子元素添加flex: 1 1；fs-1 ~ fs-6 同 h1 ~ h6 大小效果一致
``` html
<div class="dp-f1 ai-c jc-c">
  <span>left<span>
  <span class="fs-1">right<span>
<div>
```
左右布局，常见于左边图片，右边多行内容的卡片布局
``` html
<div class="dp-f ai-c">
  <div>left<div>
  <div class="fl-1">right<div>
<div>
```
上中下布局，上下固定，中间撑满并且溢出滚动
``` html
<div class="dp-f fd-c">
  <section>header<section>
  <section class="fl-1 of-a">body<section>
  <section>footer<section>
<div>
```
固定于屏幕底部, wd-100 和 wd-100vh 分别代表 width: 100% 以及 width：100vh
``` html
<body>
  <button class="pt-f bottom-l wd-100">btn<button>
<body>
```
# License

oocss is released under the [MIT](https://github.com/kunoky/oocss/blob/master/LICENSE) license.