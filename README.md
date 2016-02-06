# css-module-npm-boilerplate-webpack

[![npm version](https://badge.fury.io/js/css-module-npm-boilerplate-webpack.svg)](https://badge.fury.io/js/css-module-npm-boilerplate-webpack)

A boilerplate [css module](https://github.com/css-modules/css-modules).

Fork this and create your own reusable css module to be imported into react, deku, riot, etc... components.

![](https://raw.githubusercontent.com/StevenIseki/css-module-npm-boilerplate-webpack/master/screenshot.png)

Check out more css modules at [cssmodul.es](http://cssmodul.es)

## Compatible

CSS Modules is only compatible with camelCase. However deku and react have mappings to use *normal* class names.

This module has only camelCase classes so is compatible with:

- [css modules](https://github.com/css-modules/css-modules)
- [react-css-modules](https://github.com/gajus/react-css-modules)
- [deku-css-modules](https://github.com/StevenIseki/deku-css-modules)

## Install

`npm install css-module-npm-boilerplate-webpack --save-dev`

## Usage

`import fancyButton from 'css-module-npm-boilerplate-webpack'`

The fancy button css module has a `.button` and a color style `.blue`, `.green` or `.red`.

Add the classes to your elements to use the styles... 

**css modules**

```jsx
	return (
        <button className={styles.button + ' ' + styles.blue }>press me</button>
    );
```

**react / deku css modules**

```jsx
	return (
        <button styleName='button blue'>press me</button>
    );
```

## Example

Check out an example of using this css module [here](https://github.com/StevenIseki/css-module-npm-boilerplate-webpack/tree/master/example)

**Run it**

`cd example; npm install; npm start`

## Development

This version uses webpack to bundle the lib button.css module. For a minimal example of a css module without building with webpack use [css-module-npm-boilerplate](https://github.com/StevenIseki/css-module-npm-boilerplate)

The `\src` folder is for development. 

To build to `\lib` run:

`npm run build`

This compiles to `fancyButton.css` bundle in lib, as we do not expect all users to have the autoprefixer, postcss and postcss-modules-values plugins, they should be able to import the module as just plain css from the `\lib` so we compile it before publishing.

## License

MIT
