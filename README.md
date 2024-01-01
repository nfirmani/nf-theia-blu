### Build

```sh
# Build "dev" version of the app. Its quicker, uses less resources, 
# but the front end app is not "minified"
yarn && yarn build:dev && yarn download:plugins
```

Production applications:

```sh
# Build production version of the Eclipse Theia IDE app
yarn && yarn build && yarn download:plugins
```

### Package the Applications

```sh
yarn package:applications
# or
yarn electron package
```

### Create a Preview Electron Electron Application (without packaging it)

```sh
yarn electron package:preview
```

### Running Browser app


```sh
yarn browser start
```

and connect to <http://localhost:3000/>


### Docker Build

```sh
docker build -t theia-ide -f browser.Dockerfile .
```

You may then run this with

```sh
docker run -p=3000:3000 --rm theia-ide
```

and connect to <http://localhost:3000/>
