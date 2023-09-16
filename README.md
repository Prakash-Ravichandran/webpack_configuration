# webpack_configuration

## installation of webpack,webpack commandline interface

> > ```
> >    npm i -D webpack webpack-cli
> > ```

## Production Mode without Production

> Set build as --mode production, since we dont' have the config file yet.
>
> > ```
> >     "scripts": {
> >      "build": "webpack --mode production",
> > }
> > ```

## configuration of entries - input,output

> Specify where webpack has to start building internal dependency graph
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
