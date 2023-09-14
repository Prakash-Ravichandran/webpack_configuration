# webpack_configuration

# installation of webpack,webpack commandline interface

> > npm i -D webpack webpack-cli
> > We dont' have the config file yet, hence we select --mode production in build command

# configuration of Entries - input,output

> >

```
 entry: path.resolve(__dirname, "src/index.js"),
output: {
  path: path.resolve(__dirname, "dist"),
  filename: "bundle.js",
},

```
