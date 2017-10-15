# Webpack Demo

Webpack: input (src/index.js) -> output (dist/bundle.js)

    ./node_modules/.bin/webpack src/index.js dist/bundle.js

    or

    npm run build

    or

    webpack's Watch Mode

    or

    webpack-dev-server

    or

    webpack-dev-middleware

Adjusting your IDE: disable `safe write`

    Preferences > Appearance & Behavior > System Settings > uncheck `safe write`

Hot Module Replacement (or HMR) should only be used in development.

    webpack-dev-server --hotOnly

Tree shaking: dead-code elimination.

    use ES2015 module syntax (`import` and `export`)
    include minifier that suports dead code removal (e.g. `uglifyjs-webpack-plugin`)

Production

The goals of development and production builds differ greatly. In development, we want strong source mapping and a localhost server with live reloading or hot module replacement. In production, our goals shift to a focus on minified bundles, lighter weight source maps, and optimized assets to improve load time. With this logical separation at hand, we typically recommend writing separate webpack configurations for each environment.

    enable source mapping



Source: [webpack v3.7.1 guide](https://webpack.js.org/guides/)