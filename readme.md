# Author site for Andrew Krivák built by the New Dynamic

This site uses [Hugo](https://github.com/gohugoio/hugo), a modern framework for building websites. Hugo can be installed and run on most any system, following these [instructions](https://gohugo.io/getting-started/installing/).  This site is built and hosted at [Netlify.com](https://www.netlify.com/)

The contents of this site's themes/thenewdynamic-hugo-core-theme/src folder are used to generate CSS and javascript. You may never have to touch anything here, unless you want to more deeply customize your styles. Note that this is a submodule, and to change it you will have to fork the theme and add it, unless you have push access to the original, or, more likely, duplicate the src folder into your root directory.

## Tools

### Yarn

We use [Yarn](https://yarnpkg.com) for package managment (instead of NPM) because it's fast and generates a lock file to make dependency management more consistent. The theme's `.gitignore` file should be kept intact to make sure that all files in the `node_modules` folder are not pushed to the repository.

### Webpack

We use Webpack to manage our asset pipeline. Arguably, Webpack is overkill for this use-case, but we're using it here because once it's set up (which we've done for you), it's really easy to use. If you want to use an external script, just add it via Yarn, and reference it in main.js. You'll find instructions in the js/main.js file.

### PostCSS
PostCSS is just CSS. You'll find `postcss.config.js` in the css folder. There you'll find that we're using [`postcss-import`](https://github.com/postcss/postcss-import) which allows us import css files directly from the node_modules folder, [`postcss-cssnext`](http://cssnext.io/features/) which gives us the power to use upcoming CSS features today. If you miss Sass you can find PostCss modules for those capabilities, too.


### Tachyons

This theme uses the [Tachyons CSS Library](http://tachyons.io/). It's about 15kb gzipped, highly modular, and each class is atomic so you never have to worry about overwriting your styles. It's a great library for themes because you can make most all the style changes you need right in your layouts.

## How to Use

You'll find the commands to run in `src/package.json`.

For development, you'll need Node and Yarn installed:

```
$ cd themes/gohugo-theme-ananke/src/

$ yarn install

$ npm start

```
This will process both the postcss and scripts.

For production, instead of `npm start`, run `npm run build:production,` which will output minified versions of your files.
