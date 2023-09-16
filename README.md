# webpack_configuration

## installation of webpack,webpack cli

> Save as dev dependencies
>
> > ```
> >    npm i -D webpack webpack-cli
> > ```

## Production mode without webpack.config.js

> Set build as --mode production, since we dont' have the config file yet.
>
> > ```
> >     "scripts": {
> >      "build": "webpack --mode production",
> > }
> > ```

## configuration of entries - input,output

> Specify where webpack has to start building its internal dependency graph.<br> > [Refer Entries in detail](https://webpack.js.org/concepts#entry).
>
> > ```
> >
> > entry: path.resolve(__dirname, "src/index.js"),
> > output: {
> > path: path.resolve(__dirname, "dist"),
> > filename: "bundle.js",
> > },
> >
> > ```

## installation of sass, sass-loader,style-loader

> Save as dev dependencies
>
> > ```
> >    npm i -D sass sass-loader style-loader css-loader
> > ```

## configuration of sass-loaders,css-loaders,style-loaders

> Specify webpack to test & build the file which ends with .scss.<br> > [Refer plugins in detail](https://webpack.js.org/concepts/plugins/#usage).
>
> > ```
> >
> > module: {
> >   rules: [
> >      {
> >        test: /\.scss$/,
> >       use: ["style-loader", "css-loader", "sass-loader"],
> >       },
> >    ],
> >   },
> >
> > ```

## installation of html-webpack-plugin

> Save as dev dependencies
>
> > ```
> >    npm i -D html-webpack-plugin
> >
> > ```

## configuration of html-webpack-plugin

> Specify webpack to pick the template.html file to be generated in dist/.<br> > [Refer Loaders in detail](https://webpack.js.org/concepts/loaders/).
>
> > ```
> >
> > module: {
> >  plugins: [
> >    new HtmlWebpackPlugin({
> >     title: "Webpack App",
> >      filename: "index.html",
> >     template: "./src/template.html",
> >   }),
> > ],
> >
> > ```
