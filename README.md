# npmtest-styled-components

#### basic test coverage for  [styled-components (v1.4.5)](https://styled-components.com)  [![npm package](https://img.shields.io/npm/v/npmtest-styled-components.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-styled-components) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-styled-components.svg)](https://travis-ci.org/npmtest/node-npmtest-styled-components)

#### Visual primitives for the component age. Use the best bits of ES6 and CSS to style your apps without stress 💅

[![NPM](https://nodei.co/npm/styled-components.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/styled-components)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-styled-components/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-styled-components/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-styled-components/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-styled-components/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-styled-components/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-styled-components/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-styled-components/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-styled-components/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-styled-components/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-styled-components/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-styled-components/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-styled-components/build/test-report.html](https://npmtest.github.io/node-npmtest-styled-components/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-styled-components/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-styled-components/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-styled-components/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-styled-components/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-styled-components/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-styled-components/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-styled-components/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-styled-components/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "styled-components",
    "version": "1.4.5",
    "description": "Visual primitives for the component age. Use the best bits of ES6 and CSS to style your apps without stress 💅",
    "main": "lib/index.js",
    "typings": "typings/styled-components.d.ts",
    "jsnext:main": "dist/styled-components.es.js",
    "module": "dist/styled-components.es.js",
    "scripts": {
        "build": "npm run build:lib && npm run build:dist && npm run build:flow",
        "prebuild:lib": "rm -rf lib/*",
        "build:lib": "babel --out-dir lib src",
        "build:flow": "flow-copy-source -v -i '{**/test/*.js,**/*.test.js}' src lib",
        "prebuild:umd": "rm -rf dist/*",
        "prebuild:dist": "rm -rf dist/*",
        "build:dist": "rollup -c && rollup -c --environment PRODUCTION",
        "build:watch": "npm run build:lib -- --watch",
        "test": "mocha \"./src/**/*.test.js\" --require babel-core/register --timeout 5000",
        "test:watch": "npm run test -- --watch",
        "flow": "flow check",
        "lint": "eslint src",
        "tslint": "tslint typings/*.ts native/*.ts",
        "typescript": "tsc ./typings/styled-components-test.tsx ./typings/styled-components-native-test.tsx ./typings/themed-tests/mytheme-styled-components-test.tsx --noEmit --jsx react --target es6 --module es2015 --moduleResolution node",
        "prepublish": "npm run build",
        "lint-staged": "lint-staged",
        "dev": "node example/devServer.js"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/styled-components/styled-components.git"
    },
    "keywords": [
        "react",
        "css",
        "css-in-js",
        "styled-components"
    ],
    "author": "Glen Maddern",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/styled-components/styled-components/issues"
    },
    "homepage": "https://styled-components.com",
    "dependencies": {
        "buffer": "^5.0.2",
        "css-to-react-native": "^1.0.6",
        "fbjs": "^0.8.7",
        "inline-style-prefixer": "^2.0.5",
        "is-function": "^1.0.1",
        "is-plain-object": "^2.0.1",
        "prop-types": "^15.5.4",
        "supports-color": "^3.1.2"
    },
    "devDependencies": {
        "@types/react": "^0.14.55",
        "@types/react-native": "^0.37.5",
        "babel-cli": "^6.18.0",
        "babel-core": "^6.21.0",
        "babel-eslint": "^7.1.1",
        "babel-loader": "^6.2.10",
        "babel-plugin-add-module-exports": "^0.2.1",
        "babel-plugin-external-helpers": "^6.18.0",
        "babel-plugin-flow-react-proptypes": "^0.18.2",
        "babel-plugin-transform-class-properties": "^6.19.0",
        "babel-plugin-transform-flow-strip-types": "^6.21.0",
        "babel-plugin-transform-object-rest-spread": "^6.20.2",
        "babel-preset-env": "^1.2.1",
        "babel-preset-react": "^6.16.0",
        "chokidar": "^1.6.1",
        "danger": "^0.7.5",
        "enzyme": "^2.6.0",
        "eslint": "^3.12.2",
        "eslint-config-airbnb": "^13.0.0",
        "eslint-plugin-flowtype": "^2.29.1",
        "eslint-plugin-flowtype-errors": "^2.0.1",
        "eslint-plugin-import": "^2.2.0",
        "eslint-plugin-jsx-a11y": "^2.0.2",
        "eslint-plugin-react": "^6.8.0",
        "expect": "^1.20.2",
        "express": "^4.14.0",
        "flow-bin": "^0.37.1",
        "flow-copy-source": "^1.1.0",
        "jsdom": "^9.9.1",
        "lint-staged": "^3.2.4",
        "lodash": "^4.15.0",
        "mocha": "^3.2.0",
        "mocha-jsdom": "^1.1.0",
        "node-watch": "^0.4.1",
        "pre-commit": "^1.2.2",
        "react": "^15.4.1",
        "react-addons-test-utils": "^15.4.1",
        "react-dom": "^15.4.1",
        "react-native": "^0.39.2",
        "rollup": "^0.37.0",
        "rollup-plugin-babel": "^2.7.1",
        "rollup-plugin-commonjs": "^6.0.0",
        "rollup-plugin-flow": "^1.1.1",
        "rollup-plugin-inject": "^2.0.0",
        "rollup-plugin-json": "^2.1.0",
        "rollup-plugin-node-resolve": "^2.0.0",
        "rollup-plugin-replace": "^1.1.1",
        "rollup-plugin-uglify": "^1.0.1",
        "rollup-plugin-visualizer": "^0.1.5",
        "tslint": "^4.3.1",
        "typescript": "^2.1.5"
    },
    "peerDependencies": {
        "react": "^0.14.0 || ^15.0.0-0"
    },
    "lint-staged": {
        "*.js": [
            "eslint --fix",
            "git add"
        ]
    },
    "pre-commit": "lint-staged"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
