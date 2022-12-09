# OOCSS

简单易用的组合式css库

实际开发过程中，总是会有大量简单而又不可或缺的css被反复添加。

OOCSS没有任何依赖，复制粘贴即可使用，OOCSS包含了开发过程中最常用到的样式，通过类名组合的方式，避免了重复声明

Simple and easy to use combined CSS Library

In the actual development process, there will always be a large number of simple and indispensable CSS added repeatedly.

OOCSS does not have any dependency, and can be used by copying and pasting. OOCSS contains the most commonly used styles in the development process, and avoids repeated declarations by combining class names


[![NPM version][npm-image]][npm-url]

[npm-image]: https://img.shields.io/badge/npm-v0.0.6-blue.svg
[npm-url]: https://www.npmjs.com/package/oocss

## install

npm install oocss

## Usage

```javascript
import 'oocss'
// or 
import 'oocss/src/index.css'

// (尺寸|size) 0： 0px，s: size-s, m: size-m, l: size-l
// (颜色|color) 1-10，gray-1~gray-10, p: primary-color, s: success-color, w: warning-color, e: error-color
// (缩写|abbreviation) mgt: margin-top, pd: padding, ta: text-align
// 建议直接看代码|It is recommended to read the code directly

<div class="mgt-l pd-m tc-10 ta-c "></div>

```

```css
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
## License

oocss is released under the MIT license.