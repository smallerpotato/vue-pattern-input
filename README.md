# vue-pattern-input

A Vue2.0 Component used RegExp to limit the user's input, and works like native input element.

## Table of contents

- [Demo Build Setup](#Demo Build Setup)
- [Live Demo](#Live Demo)
- [What's included](#whats-included)
- [Quick start](#Quick start)
- [Bugs and feature requests](#bugs-and-feature-requests)
- [License](#License)

## Demo Build Setup

``` bash
# install dependencies
npm install
or
cnpm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Live Demo

Just click [Live Demo](http://htmlpreview.github.io/?https://github.com/RoamIn/vue-pattern-input/blob/master/view/demo.html).

## What's included

Within the download you'll find the following directories and files, logically grouping common assets and providing both compiled and minified variations. You'll see something like this:

```
vue-pattern-input/
├── ...
└── src/
    ├── /component
    │   └── pattern-input.vue
    └── /js
       └── ... demo ...
```

## Quick start

```
// JavaScript Part
/**
 * Component Settings
 * @param  {String} pattern     Using for: RegExp(pattern[, flags])
 * @param  {String} flags       Using for: RegExp(pattern[, flags])
 * @param  {String} replacement Using for: String.prototype.replace(regexp, replacement)
 * @param  {String} placeholder The placeholder of the input
 * @param  {String\Number} val  For v-model
 * @return {String}             
 */
setting: {
  pattern: '^[0\\D]*|\\D*', // Match string that doen't belong to the positive integer
  flags: 'g',
  replacement: '',
  placeholder: 'Oh, try out',
  val: '223'
}

// HTML Part
<pattern-input class="your-class-name"
               :pattern="setting.pattern"
               :flags="setting.flags"
               :replacement="setting.replacement"
               :placeholder="setting.placeholder"
               v-model="setting.val"></pattern-input>
```

> This setting will make user input positive integer only.

## Bugs and feature requests

Have a bug or a feature request? If your problem or idea is not addressed yet, [please open a new issue](https://github.com/RoamIn/vue-pattern-input/issues/new).

## License

Code released under the [MIT License](https://github.com/RoamIn/vue-pattern-input/blob/master/LICENSE).