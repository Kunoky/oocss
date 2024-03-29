# OOCSS

简单易用的组合式css库

实际开发过程中，总是会有大量简单而又不可或缺的css被反复添加。

OOCSS没有任何依赖，OOCSS包含了开发过程中最常用到的样式，通过类名组合的方式，避免了重复声明, 使我们不用离开html代码就可以完成样式设定。只有一个css文件，看代码更直接。

[![NPM version][npm-image]][npm-url]

[npm-image]: https://img.shields.io/badge/npm-v0.1.0-blue.svg
[npm-url]: https://www.npmjs.com/package/oocss

简体中文 | [English](./README-en.md)

## Installation

```
$ npm install oocss
```

## Usage

```javascript
import 'oocss'
// or 
import 'oocss/src/index.css'

<div class="mgt-l pd-m cl-10 ta-c "></div>
```
## Example

[dawn](https://github.com/Kunoky/dawn) | 中国大陆[加速镜像站点](https://gitee.com/Kunoky/dawn)

## Variable

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
html.dark {
  --gray-1: #2c2c2c;
  --gray-2: #454545;
  --gray-3: #5b5b5b;
  --gray-4: #7e7e7e;
  --gray-5: #adadad;
  --gray-6: #dcdcdc;
  --gray-7: #e8e8e8;
  --gray-8: #f3f3f3;
  --gray-9: #f8f8f8;
  --gray-10: #fafafa;
}
```

### 命名规则

缩写-值-伪类  
__尺寸__ 0： 0px，s: size-s, m: size-m, l: size-l  
__颜色__ 1-10，gray-1 ~ gray-10, p: primary-color, s: success-color, w: warning-color, e: error-color  

缩写通常只有2个字符，最多3个字符，一个类通常也只包含一个样式，通过样式可以很轻松的联想到类名，学习成本极低。
.mg-l { margin: var(--size-l); }  
.dp-f { display: flex; }  
.ta-c { text-align: center; }
.bgc-p { background-color: var(--primary-color); }  
.mgt-s { margin-top: var(--size-s); }  
.bdb { border-bottom: 1px solid var(--gray-5); }
.bdc-3 { border-color: var(--gray-3); }  

### demo
text-align: center;  
color: var(--gray-7);  
.cl-p-h:hover {color: var(--primary-color)};  
font-weight: bold;  
text-decoration: underline;  
padding: var(--size-s);  
.mgv-l { margin-top: var(--size-l);  margin-bottom: var(--size-l); };  
background-color: var(--gray-2);  
border: 1px solid var(--gray-5);  
box-shadow;  
cursor: pointer;
``` html
<div class="ta-c cl-7 cl-p-h fw-b td-u pd-s mgv-l bgc-2 bd bs cs-p">Hello oocss<div>
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
  <div class="fx-1">right<div>
<div>
```
上中下布局，上下固定，中间撑满并且溢出滚动，针对chrome对滚动条做出了优化
``` html
<div class="dp-f fd-c">
  <section>header<section>
  <section class="fx-1 of-a">body<section>
  <section>footer<section>
<div>
```
固定于屏幕底部, wd-100 和 wd-100vh 分别代表 width: 100% 以及 width：100vh
``` html
<body>
  <button class="pt-f bt-l wd-100">btn<button>
<body>
```
# License

oocss is released under the [MIT](https://github.com/kunoky/oocss/blob/master/LICENSE) license.