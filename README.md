#Gulp starter kit

Gulp-based build set-up for common needs.

#Concepts
- dividing source code from compiled
- separate production task
- modularity
- the edge of web technologies
- linting (code style / syntax errors checking)
- browsers live reload
- dependencies through node modules (you can install libraries through NPM and import them in your styles/scripts)

#Content

Styles: 
- Normalize.css
- PostCSS: CSSNext, PreCSS and some of Rucksack plugins (not as packs, all plugins separate) + flex bugs fixes
- Sourcemaps

Scripts: 
- Javascript: ES2015, ES2016
- Webpack 1.x (as module bundler)
- Sourcemaps

Code style checking:
- (Styles) Stylelint (standart config, csslint-missing + some sensible settings)
- (Scripts) ESLint (recommended config + airbnb config)

Images:
- sprites generator (spritesmith)
- compress images in the production build (imagemin)

Fonts (fallback: it's better to use FontSquirrel for generating fonts):
- generates TTF, WOFF, WOFF2 fonts from OTF, TTF

Browsers live reload:
- BrowserSync

#Base structure

**src/**

PostCSS (postcss/):
- main source file (main.css)
- base/:
  - vars: variables
  - tools: mixins
  - elements: base html elements styles
- objects/: OOCSS
- components/: BEM, Atomic Design
  
JavaScript (js/):
- main source file (main.js)
- modules/: folder for javascript modules

Images (img/):
- img/ - source images
- img/sprite/ - source images for sprite

Fonts (fonts/) - source fonts

**dist/**

- css/main.css - output css
- js/main.js - output js
- img/ - output images
- img/sprite.png - output sprite
- fonts/ - output fonts

#Requirements

- Node.js - latest v6.9.x LTS "Boron" is recommended
- NPM - latest version recommended
- (optional) Yarn - to use instead of NPM
- (optional) Gulp globally - latest v3.9.x recommended if you want to use gulp commands directly

#Installation

`npm install` or `yarn install`

#Usage

- `gulp` / `npm run build` / `yarn build` - build project
- `gulp watch` / `npm run watch` / `yarn watch` - watch changes
- `gulp serve` / `npm run serve` / `yarn serve` - local server that watches your changes (Browsersync)
- `gulp prod` / `npm run prod` / `yarn prod` - build production-ready code

Also, you can see subtasks in gulpfile.

#Browser support

Latest versions of the following:
- Chrome
- Edge
- Firefox
- Safari
- Opera
- Internet Explorer 9+ (Support for 9 and 10 versions is being considered to be dropped in near future)

#Related links
- [nvm](https://github.com/creationix/nvm), [Node.js](https://nodejs.org/en/), [NPM](https://www.npmjs.com/), [Yarn](https://yarnpkg.com/lang/en/)
- [Gulp](http://gulpjs.com/)
- CSS: [Normalize.css](http://necolas.github.io/normalize.css/), [OOCSS](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/), [BEM](http://getbem.com/introduction/), [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/)
- [PostCSS](http://postcss.org/): [CSSNext](http://cssnext.io/), [PreCSS](https://github.com/jonathantneal/precss), [Rucksack](https://simplaio.github.io/rucksack/), [flex bugs fixes](https://github.com/luisrudge/postcss-flexbugs-fixes)
- [Sourcemaps](https://blog.logentries.com/2014/12/what-are-javascript-source-maps/)
- JavaScript: [ES2015](https://babeljs.io/learn-es2015/), [ES2016](http://www.2ality.com/2016/01/ecmascript-2016.html), [JavaScript Modules](https://medium.freecodecamp.com/javascript-modules-a-beginner-s-guide-783f7d7a5fcc#.gckmsqgz5)
- [Module Bundling](https://medium.freecodecamp.com/javascript-modules-part-2-module-bundling-5020383cf306#.jylmhm5v0): [Webpack](https://webpack.github.io/)
- Linters: [Stylelint](https://stylelint.io/), [ESLint](http://eslint.org/)
- Images: [spritesmith](https://github.com/twolfson/gulp.spritesmith), [imagemin](https://github.com/sindresorhus/gulp-imagemin)
- [BrowserSync](https://browsersync.io/)
