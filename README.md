## JavaScript library with static helpers to render HTML with Prismic API V2

[![npm version](https://badge.fury.io/js/prismic-dom.svg)](http://badge.fury.io/js/prismic-dom)
[![Build Status](https://api.travis-ci.org/prismicio/prismic-dom.png)](https://travis-ci.org/prismicio/prismic-dom)

* The [source code](https://github.com/prismicio/prismic-dom) is on Github.
* The [Changelog](https://github.com/prismicio/prismic-dom/releases) is on Github's releases tab.
* The [API reference](https://prismicio.github.io/prismic-dom/globals.html) is on Github.

It's meant to work in pair with the prismic-javascript library, a new javascript kit for the prismic API v2 available here:
* [prismic-javascript](https://github.com/prismicio/prismic-javascript) is on Github.

### Installation

#### NPM

```sh
npm install prismic-dom --save
```

#### CDN

```
https://unpkg.com/prismic-dom
```

(You may need to adapt the version number)

#### Downloadable version

On our release page: [https://github.com/prismicio/prismic-dom/releases](https://github.com/prismicio/prismic-dom/releases).

The kit is universal, it can be used:

* Server-side with NodeJS
* Client-side as part of your build with Browserify, Webpack
* Client-side with a simple script tag

### Demo project

You can find an integration of prismic content with the new API V2 in the following project:
* [Node.js project](https://github.com/arnaudlewis/prismic-apiv2)

### Usage

With NodeJS, you can expose PrismicDOM directly in your locals to have it in your templates:
``` javascript
import PrismicDOM from 'prismic-dom';

res.locals.DOM = PrismicDOM;
```

Render a RichText:

 * As Html
```javascript
  DOM.RichText.asHtml(mydoc.data.myrichtext, linkResolver)
```

 * As Text
```javascript
  DOM.RichText.asText(mydoc.data.myrichtext)
```

Convert a Date as string from the API to an ISO Date:

```javascript
DOM.Date(mydoc.data.mydate)
```

#### Install the kit locally

Source files are in the `src/` directory. You only need [Node.js and npm](http://www.joyent.com/blog/installing-node-and-npm/)
to work on the codebase.

```
npm install
npm run dev
```

#### Documentation

Please document any new feature or bugfix using the [JSDoc](http://usejsdoc.org/) syntax. You don't need to generate the documentation, we'll do that.

If you feel an existing area of code is lacking documentation, feel free to write it; but please do so on its own branch and pull-request.

If you find existing code that is not optimally documented and wish to make it better, we really appreciate it; but you should document it on its own branch and its own pull request.

### License

This software is licensed under the Apache 2 license, quoted below.

Copyright 2013-2017 Prismic.io (http://prismic.io).

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this project except in compliance with the License. You may obtain a copy of the License at http://www.apache.org/licenses/LICENSE-2.0.

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
