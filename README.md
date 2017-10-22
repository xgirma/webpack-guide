# Webpack Demo

Webpack: input (src/index.js) -> output (dist/bundle.js)

    ./node_modules/.bin/webpack src/index.js dist/bundle.js
    npm run build
    webpack's Watch Mode
    webpack-dev-server
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
    
Code Splitting

Allows you to split your code into various bundles which can then be loaded on demand or in parallel. Control resource load prioritization, if used correctly, can have major impact on load time. Three approaches for code splitting: 

    Entry points: manually split code
    Prevent duplication: use the CommonsChunkPlugin
    Dynamic Imports: via inline finction call
    
Entry point code splitting: if there are duplicate modules, like `lodash` between entry chunks they will be included in both bundles. Can't be used to dynamically split code.  





Source: [webpack v3.7.1 guide](https://webpack.js.org/guides/)