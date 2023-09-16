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

> Specify webpack to pick the template.html file to be generated in dist/.<br> > [Refer Plugins in detail](https://webpack.js.org/concepts/plugins/#root).
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

## installation of webpack-dev-server

> Save as dev dependencies
>
> > ```
> >    npm i -D webpack-dev-server
> >
> > ```

## run webpack-dev-server

> run as
>
> > ```
> >    npm run dev
> >
> > ```

## configuration of webpack-dev-server

> Specify webpack to serve the application as live while running ``npm run dev`<br> > [Refer webpack-dev-server in detail](https://webpack.js.org/concepts/plugins/#root).
>
> > ```
> >
> > devServer: {
> >    static: {
> >      directory: path.resolve(__dirname, "dist"),
> >    },
> >    port: 3000,    // to run in 3000 port
> >    open: true,    // to open in a new tab as we run the command
> >    hot: true,
> >    compress: true,
> >    historyApiFallback: true,
> >  },
> >
> > ```

## bundle with contenthash & clean output old bundles

> set clean as true
>
> > ```
> >   output: {
> >    path: path.resolve(__dirname, "dist"),
> >    filename: "[name][contenthash].js",
> >    clean: true,
> >    }
> > ```

## debug using source-map

> source-map is useful for debug the bundle files using bundle.js.map file which is created specifically for debugging.
>
> > ```
> >    devtool: 'source-map',
> >
> > ```

## debug using babel & installation

> source-map is useful for debug the bundle files using bundle.js.map file which is created specifically for debugging.
>
> > ```
> >    npm i -D babel-loader @babel/core @babel/preset-env
> >
> > ```

## configuration of babel

> set clean as true
>
> > rules: [
> > {
> > test: /\.js$/,
> > exclude: /node_modules/,
> > use: {
> > loader: "babel-loader",
> > options: {
> > presets: ["@babel/preset-env"],
> > },
> > },
> > },
> >
> > ```
> >
> > ```
