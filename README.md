# HTML-template

This templates uses just HTML, CSS and Vanilla JavaScript (with some extra configuration TypeScript can be used as well)

## Usage

1). Watch scripts
`npm run watch`

2). Build files
`npm run build`

3). Extra scripts
Go to the `package.json` to find the individual scripts

## Optimalisations

### SEO

Some SEO best practices can be found in the `index.html`. Just update the dummy/demo text with your own text.

### Build scripts

The build scripts are scripts that will optimise your website by building (minifying and concat) your CSS and JavaScript files to a bundled file.

##### [`scripts/build-js.js`](/scripts/build-js.js)

All the (client side) scripts are getting concatenated and minified (`terser`) to one file (`bundle.min.js`) and placed in the `public/js` directory.

##### [`scripts/build-css.js`](/scripts/build-css.js)

First all the css is getting concatenated, then it's getting formatted (with cleanCSS) and eventually it's getting post processed (with autoprefixer). The bundled file will be placed in the `public/css` directory.

##### [`scripts/build-assets.js`](/scripts/build-assets.js)

It copies all the assets and place it in the `/public` folder. There is also another script named `build-img.js`. It's basically doing the same, but it has a different output directory.

### Local fonts

Local (Google) fonts are used instead of a link to the Google API. Why? It's a third-party service and browsers need to make extra requests in order to get those fonts. One request on your own server and one on the Google server. With the use of local fonts it only needs one request.

Thanks to [Google Webfonts Helper](https://google-webfonts-helper.herokuapp.com/fonts) the fonts are served locally.

## Contribution

I want to help people as much as I can with giving them the best possible html-template they can use. If you have any improvements: please let me know!

Be aware that this is still work in progress, so think could change.
