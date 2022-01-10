# BUILD-TOOLS-COURSE-ADDING-CSS-TO-OUR-BUILDS

While we import .txt files as assets, other file types often need loaders to get bundled by Webpack. Instead of a type attribute, files that use one or several loaders require a
use attribute.

CSS files use two loaders, css-loader and style-loader.css-loader takes the CSS out of a .css file and adds it to the JavaScript code. style-loader takes the output of css-loader
and puts it in a style tag in the HTML. We need both loaders and to apply css-loader first. We specify multiple loaders with an array, and Webpack applies them in reverse order.

The rule for CSS files looks like:

```
{
        test: /\.css$/i,
        use: ['style-loader','css-loader']
}
```

We can add this rule anywhere within our rules array.

In a local environment, we’d also install the loaders as developer dependencies.

```
npm install --save-dev style-loader css-loader
```

We can then import CSS files directly into our JavaScript using another form of the import statement:

```
import './style.css';
import Text from './example.txt';
document.querySelector('h1').innerHTML = Text;
```

```
npm install --save-dev webpack-dev-server
```

```
npm run build
```

```
npm run start
```
