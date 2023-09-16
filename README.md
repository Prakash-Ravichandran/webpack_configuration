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

# configuration of Entries - input,output

> Set build as --mode production, since we dont' have the config file yet.
>
> > ```
> > entry: path.resolve(**dirname, "src/index.js"),
> > output: {
> > path: path.resolve(**dirname, "dist"),
> > filename: "bundle.js",
> > },
> >
> > ```
