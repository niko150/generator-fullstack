# Full-stack generator [![NPM version][npm-version-image]][npm-version-url] [![NPM Downloads][npm-downloads-image]][npm-downloads-url] [![Dependency Status][daviddm-image]][daviddm-url] [![License][license-image]][license-url]

## Installation

First, install [Yeoman](http://yeoman.io) and the Full-stack generator using [npm](https://www.npmjs.com/):

```bash
npm i -g yo generator-fullstack
```

Then generate your new project:

```bash
yo fullstack
```

## Information

This is a generator providing the following options...

JavaScript:

- Vanilla
- Vue.js (incl/ single file components, vue-router & vue-i18n)
- React

CSS:
- Stylus
- Sass
- SCSS

...based upon a foundation of the following:

- Node.js / Express on the backend
- Pug templating language
- npm for package management (Yarn will be used if available)
- dotenv for enviromment variables
- Babel transpilation for ES2015 & ES2016 down to ES5 and optionally a few useful polyfills (detailed below)

### Legacy Browsers

During setup you will be asked for your targeted browser support. "Modern" is defined as the latest versions of Chrome, Firefox, Edge, and Safari. "Legacy" is summarily defined as IE9+.

The following JS polyfills are included in legacy builds:

- Promise - no native support in IE
- Element.classList - no native support below IE10, and only partial support in IE10 & IE11
- Window.matchMedia() - no native support below IE10
- String.prototype.includes() - no native support in IE, Opera
- Array.from() - no native support in IE, Opera

If you select the modern browsers configuration these polyfills will not be included.

For now, Babel transpilation down to ES5 will be included in all builds.

### Directory Setup

Following generation you will end up with something like this, dependent upon the options you selected:

```
.
├── app/
│   └── routes.js
│   └── server.js
│   └── src/
│       └── modules/
│           └── [etc].js
│       └── styles/
│           └── [etc].styl
│       └── client.js
│   └── static/
│       └── humans.txt
│       └── img/
│   └── views/
│       └── [etc].pug
├── build/
│   └── webpack.base.config.js
│   └── webpack.development.config.js
│   └── webpack.production.js
├── .babelrc
├── .editorconfig
├── .env.example
├── .eslintrc
├── .gitignore
├── CHANGELOG.md
├── README.md
├── package.json
```

## Help

Once generation is complete you should check the generated README for a quick setup guide. The project should immediately run and function as if you'd painstakingly scaffolded it out yourself. If for any reason that doesn't happen, please file an issue detailing the options you selected, the error that was thrown (if any), and any further pertinent information.

[npm-version-image]: https://badge.fury.io/js/generator-fullstack.svg
[npm-version-url]: https://npmjs.org/package/generator-fullstack
[npm-downloads-image]: https://img.shields.io/npm/dm/generator-fullstack.svg
[npm-downloads-url]: https://npmjs.org/package/generator-fullstack
[license-image]: https://img.shields.io/npm/l/generator-fullstack.svg
[license-url]: https://npmjs.org/package/generator-fullstack
[daviddm-image]: https://img.shields.io/david/samhh/generator-fullstack.svg
[daviddm-url]: https://david-dm.org/samhh/generator-fullstack
