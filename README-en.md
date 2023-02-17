# OOCSS

Simple and easy to use combined CSS Library

In the actual development process, there will always be a large number of simple and indispensable CSS added repeatedly.

OOCSS does not have any dependency, OOCSS contains the most commonly used styles in the development process, and avoids repeated declarations by combining class names，So that we can complete the style setting without leaving the html code


[![NPM version][npm-image]][npm-url]

[npm-image]: https://img.shields.io/badge/npm-v0.0.7-blue.svg
[npm-url]: https://www.npmjs.com/package/oocss

[简体中文](./README.md) | English

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
/** The uniform use of variables is extremely convenient to modify and maintaining consistency */
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

Abbreviation-Value-Pseudo Class  

__size__ 0： 0px，s: size-s, m: size-m, l: size-l  
__color__ 1-10，gray-1 ~ gray-10, p: primary-color, s: success-color, w: warning-color, e: error-color  

Abbreviations usually have only 2 characters, and a class usually contains only one style.  
.mg-l { margin: var(--size-l); }  
.dp-f { display: flex; }  
.ta-c { text-align: center; }

Except for top, bottom, left and right, there are no abbreviations. At present, the abbreviations are up to 3 characters, which is quite concise.  
.bgc-p { background-color: var(--primary-color); }  
.mgt-s { margin-top: var(--size-s); }  
.bdb { border-bottom: 1px solid var(--gray-5); }
.bdc-3 { border-color: var(--gray-3); }  

### demo
text-align: center;  
color: var(--gray-7);  
.tc-p-h:hover {color: var(--primary-color)};  
font-weight: bold;  
text-decoration: underline;  
padding: var(--size-s);  
.mgv-l { margin-top: var(--size-l);  margin-bottom: var(--size-l); };  
background-color: var(--gray-2);  
border: 1px solid var(--gray-5);  
box-shadow;  
cursor: pointer;
``` html
<div class="ta-c tc-7 tc-p-h fw-b td-u pd-s mgv-l bgc-2 bd bsd cs-p">Hello oocss<div>
```
Flex bisects the space and centers horizontally and vertically. 'dp-f1' will setting display: flex and add 'flex: 1 1' to all child elements; 'fs-1 ~ fs-6' has the same size effect as h1 ~ h6 tags
``` html
<div class="dp-f1 ai-c jc-c">
  <span>left<span>
  <span class="fs-1">right<span>
<div>
```
Left and right layout, common in the card layout of the left picture and multiple lines of content on the right
``` html
<div class="dp-f ai-c">
  <div>left<div>
  <div class="fl-1">right<div>
<div>
```
Top, middle and bottom layout, fixed top and bottom, full in the middle and overflow scrollable
``` html
<div class="dp-f fd-c">
  <section>header<section>
  <section class="fl-1 of-a">body<section>
  <section>footer<section>
<div>
```
Fixed at the bottom of the screen, wd-100 and wd-100vh represent width: 100% and width: 100vh respectively
``` html
<body>
  <button class="pt-f bottom-l wd-100">btn<button>
<body>
```
# License

oocss is released under the [MIT](https://github.com/kunoky/oocss/master/LICENSE) license.