# Eslint

`<auro-eslint>` is a [HTML custom element](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements) for the purpose of ...

## UI development browser support

For the most up to date information on [UI development browser support](https://auro.alaskaair.com/support/browsersSupport)

## Install

[![Build Status](https://img.shields.io/github/workflow/status/AlaskaAirlines/auro-eslint/Test%20and%20publish?branch=master&style=for-the-badge)](https://github.com/AlaskaAirlines/auro-eslint/actions?query=workflow%3A%22test+and+publish%22)
[![See it on NPM!](https://img.shields.io/npm/v/@aurodesignsystem/auro-eslint?style=for-the-badge&color=orange)](https://www.npmjs.com/package/@aurodesignsystem/auro-eslint)
[![License](https://img.shields.io/npm/l/@aurodesignsystem/auro-eslint?color=blue&style=for-the-badge)](https://www.apache.org/licenses/LICENSE-2.0)

```shell
$ npm i @aurodesignsystem/auro-eslint
```

Installing as a direct, dev or peer dependency is up to the user installing the package. If you are unsure as to what type of dependency you should use, consider reading this [stack overflow](https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies) answer.

### Design Token CSS Custom Property dependency

The use of any Auro custom element has a dependency on the [Auro Design Tokens](https://auro.alaskaair.com/getting-started/developers/design-tokens).

### CSS Custom Property fallbacks

[CSS custom properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) are [not supported](https://auro.alaskaair.com/support/custom-properties) in older browsers. For this, fallback properties are pre-generated and included with the npm.

Any update to the Auro Design Tokens will be immediately reflected with browsers that support CSS custom properties, legacy browsers will require updated components with pre-generated fallback properties.

### Define dependency in project component

Defining the component dependency within each component that is using the `<auro-eslint>` component.

```javascript
import "@aurodesignsystem/auro-eslint";
```

**Reference component in HTML**

```html
<auro-eslint>Hello World</auro-eslint>
```

## Install bundled assets from CDN

In cases where the project is not able to process JS assets, there are pre-processed assets available for use. Two bundles are available -- `auro-eslint__bundled.js` for modern browsers and `auro-eslint__bundled.es5.js` for legacy browsers (including IE11).

Since the legacy bundle includes many polyfills that are not needed by modern browsers, we recommend you load these bundles using [differential serving](https://philipwalton.com/articles/deploying-es2015-code-in-production-today/) so that the browser only loads the bundle it needs. To accomplish this, the script tag for the modern bundle should have `type="module"` and the script tag for the legacy bundle should have the `nomodule` attribute. See the example below.

### Bundle example code

**NOTE:** Be sure to replace `@latest` in the URL with the version of the asset you want. @latest is NOT aware of any MAJOR releases, use at your own risk.

```html
<link rel="stylesheet" href="https://unpkg.com/@alaskaairux/design-tokens@latest/dist/tokens/CSSCustomProperties.css" />
<link rel="stylesheet" href="https://unpkg.com/@alaskaairux/webcorestylesheets@latest/dist/bundled/essentials.css" />

<script src="https://unpkg.com/@alaskaairux/auro-eslint@latest/dist/auro-eslint__bundled.js" type="module"></script>
<script src="https://unpkg.com/@alaskaairux/auro-eslint@latest/dist/auro-eslint__bundled.es5.js" nomodule></script>
```

## auro-eslint use cases

The `<auro-eslint>` element should be used in situations where users may:

* ...
* ...
* ...

## API Code Examples

Default auro-eslint

```html
<auro-eslint>Hello World</auro-eslint>
```

## Development

In order to develop against this project, if you are not part of the core team, you will be required to fork the project prior to submitting a pull request.

Please be sure to review the [contribution guidelines](https://auro.alaskaair.com/getting-started/developers/contributing) for this project. Please make sure to **pay special attention** to the **conventional commits** section of the document.

### Start development environment

Once the project has been cloned to your local resource and you have installed all the dependencies you will need to open two different shell sessions. One is for the **npm tasks**, the second is to run the **server**.

```shell
// shell terminal one
$ npm run dev

// shell terminal two
$ npm run serve
```

Open [localhost:8000](http://localhost:8000/)

### Writing SCSS
Auro has implemented [CSScomb](https://www.npmjs.com/package/csscomb) for style formatting enforcement in addition to the [linting requirements](https://auro.alaskaair.com/webcorestylesheets/linter).

The build process will auto-execute the CSScomb formatter as part of the pre-commit workflow prior to executing the automated test scripts. If your component includes more than a trivial amount of custom CSS you may find it helpful to run the CSSComb formatter during your regular development. You can run `npm run cssComb` to execute the process manually.

Additionally, you may choose to install a CSScomb extension for your IDE of choice. These extensions allow for simple format-on-save and keybind trigger of CSScomb execution. These extensions will automatically use the config file located at the root of the project template and format your styles in compliance with Auro guidelines. Refer to your chosen IDE's documentation for how to search for and install extensions.

See [the styleguide documentation](https://auro.alaskaair.com/webcorestylesheets/guidelines) for more details about how to properly format your styles.

### Testing
Automated tests are required for every Auro component. See `.\test\auro-eslint.test.js` for the tests for this component. Run `npm test` to run the tests and check code coverage. Tests must pass and meet a certain coverage threshold to commit. See [the testing documentation](https://auro.alaskaair.com/support/tests) for more details.

### Demo deployment

To deploy a demo version of the component for review, run `npm run demo:build` to create a `./build` directory that can be pushed to any static server.

<small>Built from WC-Generator v2.11.0</small>
