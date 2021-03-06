# tachyons-flexbox 2.1.0

Flexbox CSS module for Tachyons

#### Stats

1662 | 184 | 516
---|---|---
bytes | selectors | declarations

## Installation

#### With [npm](https://npmjs.com)

```
npm install --save-dev tachyons-flexbox
```

Learn more about using css installed with npm:
* https://webpack.github.io/docs/stylesheets.html
* https://github.com/defunctzombie/npm-css

#### With Git

http:
```
git clone https://github.com/tachyons-css/tachyons-flexbox
```

ssh:
```
git clone git@github.com:tachyons-css/tachyons-flexbox.git
```

## Usage

#### Using with [Postcss](https://github.com/postcss/postcss)

Import the css module

```css
@import "tachyons-flexbox";
```

Then process the css using the [`tachyons-cli`](https://github.com/tachyons-css/tachyons-cli)

```sh
$ npm i -g tachyons-cli
$ tachyons path/to/css-file.css > dist/t.css
```

#### Using the css

##### CDN
The easiest and most simple way to use the css is to use the cdn hosted version. Include it in the head of your html with:

```
<link rel="stylesheet" href="http://unpkg.com/tachyons-flexbox@2.1.0/css/tachyons-flexbox.min.css" />
```

##### Locally
The built css is located in the `css` directory. It contains an unminified and minified version.
You can either cut and paste that css or link to it directly in your html.

```html
<link rel="stylesheet" href="path/to/module/css/tachyons-flexbox">
```

#### Development

The source css files can be found in the `src` directory.
Running `$ npm start` will process the source css and place the built css in the `css` directory.

## The css

```css
/*

  FLEXBOX

  Media Query Extensions:
   -ns = not-small
   -m  = medium
   -l  = large

*/
.flex { display: -webkit-box; display: -ms-flexbox; display: flex; }
.inline-flex { display: -webkit-inline-box; display: -ms-inline-flexbox; display: inline-flex; }
/* 1. Fix for Chrome 44 bug.
 * https://code.google.com/p/chromium/issues/detail?id=506893 */
.flex-auto { -webkit-box-flex: 1; -ms-flex: 1 1 auto; flex: 1 1 auto; min-width: 0; /* 1 */ min-height: 0; /* 1 */ }
.flex-none { -webkit-box-flex: 0; -ms-flex: none; flex: none; }
.flex-column { -webkit-box-orient: vertical; -webkit-box-direction: normal; -ms-flex-direction: column; flex-direction: column; }
.flex-row { -webkit-box-orient: horizontal; -webkit-box-direction: normal; -ms-flex-direction: row; flex-direction: row; }
.flex-wrap { -ms-flex-wrap: wrap; flex-wrap: wrap; }
.flex-nowrap { -ms-flex-wrap: nowrap; flex-wrap: nowrap; }
.flex-wrap-reverse { -ms-flex-wrap: wrap-reverse; flex-wrap: wrap-reverse; }
.flex-column-reverse { -webkit-box-orient: vertical; -webkit-box-direction: reverse; -ms-flex-direction: column-reverse; flex-direction: column-reverse; }
.flex-row-reverse { -webkit-box-orient: horizontal; -webkit-box-direction: reverse; -ms-flex-direction: row-reverse; flex-direction: row-reverse; }
.items-start { -webkit-box-align: start; -ms-flex-align: start; align-items: flex-start; }
.items-end { -webkit-box-align: end; -ms-flex-align: end; align-items: flex-end; }
.items-center { -webkit-box-align: center; -ms-flex-align: center; align-items: center; }
.items-baseline { -webkit-box-align: baseline; -ms-flex-align: baseline; align-items: baseline; }
.items-stretch { -webkit-box-align: stretch; -ms-flex-align: stretch; align-items: stretch; }
.self-start { -ms-flex-item-align: start; align-self: flex-start; }
.self-end { -ms-flex-item-align: end; align-self: flex-end; }
.self-center { -ms-flex-item-align: center; -ms-grid-row-align: center; align-self: center; }
.self-baseline { -ms-flex-item-align: baseline; align-self: baseline; }
.self-stretch { -ms-flex-item-align: stretch; -ms-grid-row-align: stretch; align-self: stretch; }
.justify-start { -webkit-box-pack: start; -ms-flex-pack: start; justify-content: flex-start; }
.justify-end { -webkit-box-pack: end; -ms-flex-pack: end; justify-content: flex-end; }
.justify-center { -webkit-box-pack: center; -ms-flex-pack: center; justify-content: center; }
.justify-between { -webkit-box-pack: justify; -ms-flex-pack: justify; justify-content: space-between; }
.justify-around { -ms-flex-pack: distribute; justify-content: space-around; }
.content-start { -ms-flex-line-pack: start; align-content: flex-start; }
.content-end { -ms-flex-line-pack: end; align-content: flex-end; }
.content-center { -ms-flex-line-pack: center; align-content: center; }
.content-between { -ms-flex-line-pack: justify; align-content: space-between; }
.content-around { -ms-flex-line-pack: distribute; align-content: space-around; }
.content-stretch { -ms-flex-line-pack: stretch; align-content: stretch; }
.order-0 { -webkit-box-ordinal-group: 1; -ms-flex-order: 0; order: 0; }
.order-1 { -webkit-box-ordinal-group: 2; -ms-flex-order: 1; order: 1; }
.order-2 { -webkit-box-ordinal-group: 3; -ms-flex-order: 2; order: 2; }
.order-3 { -webkit-box-ordinal-group: 4; -ms-flex-order: 3; order: 3; }
.order-4 { -webkit-box-ordinal-group: 5; -ms-flex-order: 4; order: 4; }
.order-5 { -webkit-box-ordinal-group: 6; -ms-flex-order: 5; order: 5; }
.order-6 { -webkit-box-ordinal-group: 7; -ms-flex-order: 6; order: 6; }
.order-7 { -webkit-box-ordinal-group: 8; -ms-flex-order: 7; order: 7; }
.order-8 { -webkit-box-ordinal-group: 9; -ms-flex-order: 8; order: 8; }
.order-last { -webkit-box-ordinal-group: 100000; -ms-flex-order: 99999; order: 99999; }
.flex-grow-0 { -webkit-box-flex: 0; -ms-flex-positive: 0; flex-grow: 0; }
.flex-grow-1 { -webkit-box-flex: 1; -ms-flex-positive: 1; flex-grow: 1; }
.flex-shrink-0 { -ms-flex-negative: 0; flex-shrink: 0; }
.flex-shrink-1 { -ms-flex-negative: 1; flex-shrink: 1; }
@media screen and (min-width: 30em) {
 .flex-ns { display: -webkit-box; display: -ms-flexbox; display: flex; }
 .inline-flex-ns { display: -webkit-inline-box; display: -ms-inline-flexbox; display: inline-flex; }
 .flex-auto-ns { -webkit-box-flex: 1; -ms-flex: 1 1 auto; flex: 1 1 auto; min-width: 0; /* 1 */ min-height: 0; /* 1 */ }
 .flex-none-ns { -webkit-box-flex: 0; -ms-flex: none; flex: none; }
 .flex-column-ns { -webkit-box-orient: vertical; -webkit-box-direction: normal; -ms-flex-direction: column; flex-direction: column; }
 .flex-row-ns { -webkit-box-orient: horizontal; -webkit-box-direction: normal; -ms-flex-direction: row; flex-direction: row; }
 .flex-wrap-ns { -ms-flex-wrap: wrap; flex-wrap: wrap; }
 .flex-nowrap-ns { -ms-flex-wrap: nowrap; flex-wrap: nowrap; }
 .flex-wrap-reverse-ns { -ms-flex-wrap: wrap-reverse; flex-wrap: wrap-reverse; }
 .flex-column-reverse-ns { -webkit-box-orient: vertical; -webkit-box-direction: reverse; -ms-flex-direction: column-reverse; flex-direction: column-reverse; }
 .flex-row-reverse-ns { -webkit-box-orient: horizontal; -webkit-box-direction: reverse; -ms-flex-direction: row-reverse; flex-direction: row-reverse; }
 .items-start-ns { -webkit-box-align: start; -ms-flex-align: start; align-items: flex-start; }
 .items-end-ns { -webkit-box-align: end; -ms-flex-align: end; align-items: flex-end; }
 .items-center-ns { -webkit-box-align: center; -ms-flex-align: center; align-items: center; }
 .items-baseline-ns { -webkit-box-align: baseline; -ms-flex-align: baseline; align-items: baseline; }
 .items-stretch-ns { -webkit-box-align: stretch; -ms-flex-align: stretch; align-items: stretch; }
 .self-start-ns { -ms-flex-item-align: start; align-self: flex-start; }
 .self-end-ns { -ms-flex-item-align: end; align-self: flex-end; }
 .self-center-ns { -ms-flex-item-align: center; -ms-grid-row-align: center; align-self: center; }
 .self-baseline-ns { -ms-flex-item-align: baseline; align-self: baseline; }
 .self-stretch-ns { -ms-flex-item-align: stretch; -ms-grid-row-align: stretch; align-self: stretch; }
 .justify-start-ns { -webkit-box-pack: start; -ms-flex-pack: start; justify-content: flex-start; }
 .justify-end-ns { -webkit-box-pack: end; -ms-flex-pack: end; justify-content: flex-end; }
 .justify-center-ns { -webkit-box-pack: center; -ms-flex-pack: center; justify-content: center; }
 .justify-between-ns { -webkit-box-pack: justify; -ms-flex-pack: justify; justify-content: space-between; }
 .justify-around-ns { -ms-flex-pack: distribute; justify-content: space-around; }
 .content-start-ns { -ms-flex-line-pack: start; align-content: flex-start; }
 .content-end-ns { -ms-flex-line-pack: end; align-content: flex-end; }
 .content-center-ns { -ms-flex-line-pack: center; align-content: center; }
 .content-between-ns { -ms-flex-line-pack: justify; align-content: space-between; }
 .content-around-ns { -ms-flex-line-pack: distribute; align-content: space-around; }
 .content-stretch-ns { -ms-flex-line-pack: stretch; align-content: stretch; }
 .order-0-ns { -webkit-box-ordinal-group: 1; -ms-flex-order: 0; order: 0; }
 .order-1-ns { -webkit-box-ordinal-group: 2; -ms-flex-order: 1; order: 1; }
 .order-2-ns { -webkit-box-ordinal-group: 3; -ms-flex-order: 2; order: 2; }
 .order-3-ns { -webkit-box-ordinal-group: 4; -ms-flex-order: 3; order: 3; }
 .order-4-ns { -webkit-box-ordinal-group: 5; -ms-flex-order: 4; order: 4; }
 .order-5-ns { -webkit-box-ordinal-group: 6; -ms-flex-order: 5; order: 5; }
 .order-6-ns { -webkit-box-ordinal-group: 7; -ms-flex-order: 6; order: 6; }
 .order-7-ns { -webkit-box-ordinal-group: 8; -ms-flex-order: 7; order: 7; }
 .order-8-ns { -webkit-box-ordinal-group: 9; -ms-flex-order: 8; order: 8; }
 .order-last-ns { -webkit-box-ordinal-group: 100000; -ms-flex-order: 99999; order: 99999; }
 .flex-grow-0-ns { -webkit-box-flex: 0; -ms-flex-positive: 0; flex-grow: 0; }
 .flex-grow-1-ns { -webkit-box-flex: 1; -ms-flex-positive: 1; flex-grow: 1; }
 .flex-shrink-0-ns { -ms-flex-negative: 0; flex-shrink: 0; }
 .flex-shrink-1-ns { -ms-flex-negative: 1; flex-shrink: 1; }
}
@media screen and (min-width: 30em) and (max-width: 60em) {
 .flex-m { display: -webkit-box; display: -ms-flexbox; display: flex; }
 .inline-flex-m { display: -webkit-inline-box; display: -ms-inline-flexbox; display: inline-flex; }
 .flex-auto-m { -webkit-box-flex: 1; -ms-flex: 1 1 auto; flex: 1 1 auto; min-width: 0; /* 1 */ min-height: 0; /* 1 */ }
 .flex-none-m { -webkit-box-flex: 0; -ms-flex: none; flex: none; }
 .flex-column-m { -webkit-box-orient: vertical; -webkit-box-direction: normal; -ms-flex-direction: column; flex-direction: column; }
 .flex-row-m { -webkit-box-orient: horizontal; -webkit-box-direction: normal; -ms-flex-direction: row; flex-direction: row; }
 .flex-wrap-m { -ms-flex-wrap: wrap; flex-wrap: wrap; }
 .flex-nowrap-m { -ms-flex-wrap: nowrap; flex-wrap: nowrap; }
 .flex-wrap-reverse-m { -ms-flex-wrap: wrap-reverse; flex-wrap: wrap-reverse; }
 .flex-column-reverse-m { -webkit-box-orient: vertical; -webkit-box-direction: reverse; -ms-flex-direction: column-reverse; flex-direction: column-reverse; }
 .flex-row-reverse-m { -webkit-box-orient: horizontal; -webkit-box-direction: reverse; -ms-flex-direction: row-reverse; flex-direction: row-reverse; }
 .items-start-m { -webkit-box-align: start; -ms-flex-align: start; align-items: flex-start; }
 .items-end-m { -webkit-box-align: end; -ms-flex-align: end; align-items: flex-end; }
 .items-center-m { -webkit-box-align: center; -ms-flex-align: center; align-items: center; }
 .items-baseline-m { -webkit-box-align: baseline; -ms-flex-align: baseline; align-items: baseline; }
 .items-stretch-m { -webkit-box-align: stretch; -ms-flex-align: stretch; align-items: stretch; }
 .self-start-m { -ms-flex-item-align: start; align-self: flex-start; }
 .self-end-m { -ms-flex-item-align: end; align-self: flex-end; }
 .self-center-m { -ms-flex-item-align: center; -ms-grid-row-align: center; align-self: center; }
 .self-baseline-m { -ms-flex-item-align: baseline; align-self: baseline; }
 .self-stretch-m { -ms-flex-item-align: stretch; -ms-grid-row-align: stretch; align-self: stretch; }
 .justify-start-m { -webkit-box-pack: start; -ms-flex-pack: start; justify-content: flex-start; }
 .justify-end-m { -webkit-box-pack: end; -ms-flex-pack: end; justify-content: flex-end; }
 .justify-center-m { -webkit-box-pack: center; -ms-flex-pack: center; justify-content: center; }
 .justify-between-m { -webkit-box-pack: justify; -ms-flex-pack: justify; justify-content: space-between; }
 .justify-around-m { -ms-flex-pack: distribute; justify-content: space-around; }
 .content-start-m { -ms-flex-line-pack: start; align-content: flex-start; }
 .content-end-m { -ms-flex-line-pack: end; align-content: flex-end; }
 .content-center-m { -ms-flex-line-pack: center; align-content: center; }
 .content-between-m { -ms-flex-line-pack: justify; align-content: space-between; }
 .content-around-m { -ms-flex-line-pack: distribute; align-content: space-around; }
 .content-stretch-m { -ms-flex-line-pack: stretch; align-content: stretch; }
 .order-0-m { -webkit-box-ordinal-group: 1; -ms-flex-order: 0; order: 0; }
 .order-1-m { -webkit-box-ordinal-group: 2; -ms-flex-order: 1; order: 1; }
 .order-2-m { -webkit-box-ordinal-group: 3; -ms-flex-order: 2; order: 2; }
 .order-3-m { -webkit-box-ordinal-group: 4; -ms-flex-order: 3; order: 3; }
 .order-4-m { -webkit-box-ordinal-group: 5; -ms-flex-order: 4; order: 4; }
 .order-5-m { -webkit-box-ordinal-group: 6; -ms-flex-order: 5; order: 5; }
 .order-6-m { -webkit-box-ordinal-group: 7; -ms-flex-order: 6; order: 6; }
 .order-7-m { -webkit-box-ordinal-group: 8; -ms-flex-order: 7; order: 7; }
 .order-8-m { -webkit-box-ordinal-group: 9; -ms-flex-order: 8; order: 8; }
 .order-last-m { -webkit-box-ordinal-group: 100000; -ms-flex-order: 99999; order: 99999; }
 .flex-grow-0-m { -webkit-box-flex: 0; -ms-flex-positive: 0; flex-grow: 0; }
 .flex-grow-1-m { -webkit-box-flex: 1; -ms-flex-positive: 1; flex-grow: 1; }
 .flex-shrink-0-m { -ms-flex-negative: 0; flex-shrink: 0; }
 .flex-shrink-1-m { -ms-flex-negative: 1; flex-shrink: 1; }
}
@media screen and (min-width: 60em) {
 .flex-l { display: -webkit-box; display: -ms-flexbox; display: flex; }
 .inline-flex-l { display: -webkit-inline-box; display: -ms-inline-flexbox; display: inline-flex; }
 .flex-auto-l { -webkit-box-flex: 1; -ms-flex: 1 1 auto; flex: 1 1 auto; min-width: 0; /* 1 */ min-height: 0; /* 1 */ }
 .flex-none-l { -webkit-box-flex: 0; -ms-flex: none; flex: none; }
 .flex-column-l { -webkit-box-orient: vertical; -webkit-box-direction: normal; -ms-flex-direction: column; flex-direction: column; }
 .flex-row-l { -webkit-box-orient: horizontal; -webkit-box-direction: normal; -ms-flex-direction: row; flex-direction: row; }
 .flex-wrap-l { -ms-flex-wrap: wrap; flex-wrap: wrap; }
 .flex-nowrap-l { -ms-flex-wrap: nowrap; flex-wrap: nowrap; }
 .flex-wrap-reverse-l { -ms-flex-wrap: wrap-reverse; flex-wrap: wrap-reverse; }
 .flex-column-reverse-l { -webkit-box-orient: vertical; -webkit-box-direction: reverse; -ms-flex-direction: column-reverse; flex-direction: column-reverse; }
 .flex-row-reverse-l { -webkit-box-orient: horizontal; -webkit-box-direction: reverse; -ms-flex-direction: row-reverse; flex-direction: row-reverse; }
 .items-start-l { -webkit-box-align: start; -ms-flex-align: start; align-items: flex-start; }
 .items-end-l { -webkit-box-align: end; -ms-flex-align: end; align-items: flex-end; }
 .items-center-l { -webkit-box-align: center; -ms-flex-align: center; align-items: center; }
 .items-baseline-l { -webkit-box-align: baseline; -ms-flex-align: baseline; align-items: baseline; }
 .items-stretch-l { -webkit-box-align: stretch; -ms-flex-align: stretch; align-items: stretch; }
 .self-start-l { -ms-flex-item-align: start; align-self: flex-start; }
 .self-end-l { -ms-flex-item-align: end; align-self: flex-end; }
 .self-center-l { -ms-flex-item-align: center; -ms-grid-row-align: center; align-self: center; }
 .self-baseline-l { -ms-flex-item-align: baseline; align-self: baseline; }
 .self-stretch-l { -ms-flex-item-align: stretch; -ms-grid-row-align: stretch; align-self: stretch; }
 .justify-start-l { -webkit-box-pack: start; -ms-flex-pack: start; justify-content: flex-start; }
 .justify-end-l { -webkit-box-pack: end; -ms-flex-pack: end; justify-content: flex-end; }
 .justify-center-l { -webkit-box-pack: center; -ms-flex-pack: center; justify-content: center; }
 .justify-between-l { -webkit-box-pack: justify; -ms-flex-pack: justify; justify-content: space-between; }
 .justify-around-l { -ms-flex-pack: distribute; justify-content: space-around; }
 .content-start-l { -ms-flex-line-pack: start; align-content: flex-start; }
 .content-end-l { -ms-flex-line-pack: end; align-content: flex-end; }
 .content-center-l { -ms-flex-line-pack: center; align-content: center; }
 .content-between-l { -ms-flex-line-pack: justify; align-content: space-between; }
 .content-around-l { -ms-flex-line-pack: distribute; align-content: space-around; }
 .content-stretch-l { -ms-flex-line-pack: stretch; align-content: stretch; }
 .order-0-l { -webkit-box-ordinal-group: 1; -ms-flex-order: 0; order: 0; }
 .order-1-l { -webkit-box-ordinal-group: 2; -ms-flex-order: 1; order: 1; }
 .order-2-l { -webkit-box-ordinal-group: 3; -ms-flex-order: 2; order: 2; }
 .order-3-l { -webkit-box-ordinal-group: 4; -ms-flex-order: 3; order: 3; }
 .order-4-l { -webkit-box-ordinal-group: 5; -ms-flex-order: 4; order: 4; }
 .order-5-l { -webkit-box-ordinal-group: 6; -ms-flex-order: 5; order: 5; }
 .order-6-l { -webkit-box-ordinal-group: 7; -ms-flex-order: 6; order: 6; }
 .order-7-l { -webkit-box-ordinal-group: 8; -ms-flex-order: 7; order: 7; }
 .order-8-l { -webkit-box-ordinal-group: 9; -ms-flex-order: 8; order: 8; }
 .order-last-l { -webkit-box-ordinal-group: 100000; -ms-flex-order: 99999; order: 99999; }
 .flex-grow-0-l { -webkit-box-flex: 0; -ms-flex-positive: 0; flex-grow: 0; }
 .flex-grow-1-l { -webkit-box-flex: 1; -ms-flex-positive: 1; flex-grow: 1; }
 .flex-shrink-0-l { -ms-flex-negative: 0; flex-shrink: 0; }
 .flex-shrink-1-l { -ms-flex-negative: 1; flex-shrink: 1; }
}
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Authors

* [mrmrs](http://mrmrs.io)
* [johno](http://johnotander.com)

## License

ISC

