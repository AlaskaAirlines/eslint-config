# Auro Eslint Setup

`auro-eslint-config` is a [pre-configured set of code style rules](https://eslint.org/) for the purpose of maintaining code quality and consistency between projects.

## Install

[![Build Status](https://img.shields.io/github/workflow/status/AlaskaAirlines/auro-eslint-config/Test%20and%20publish?branch=master&style=for-the-badge)](https://github.com/AlaskaAirlines/auro-eslint-config/actions?query=workflow%3A%22test+and+publish%22)
[![See it on NPM!](https://img.shields.io/npm/v/@aurodesignsystem/eslint-config?style=for-the-badge&color=orange)](https://www.npmjs.com/package/@aurodesignsystem/eslint-config)
[![License](https://img.shields.io/npm/l/@aurodesignsystem/eslint-config?color=blue&style=for-the-badge)](https://www.apache.org/licenses/LICENSE-2.0)

```shell
$ npm i @aurodesignsystem/eslint-config
```

Installing as a direct, dev or peer dependency is up to the user installing the package. If you are unsure as to what type of dependency you should use, consider reading this [stack overflow](https://stackoverflow.com/questions/18875674/whats-the-difference-between-dependencies-devdependencies-and-peerdependencies) answer.

### Add .eslintrc file

At the root of your project, create a `.eslintrc` file with the following code:

```js
{
  "extends": [
    "@aurodesignsystem/eslint-config"
  ]
}
```

## Development

In order to develop against this project, if you are not part of the core team, you will be required to fork the project prior to submitting a pull request.

Please be sure to review the [contribution guidelines](https://auro.alaskaair.com/getting-started/developers/contributing) for this project. Please make sure to **pay special attention** to the **conventional commits** section of the document.
