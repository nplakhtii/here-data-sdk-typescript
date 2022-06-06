# HERE Data SDK for TypeScript

HERE Data SDK for TypeScript is a TypeScript client for the <a href="https://platform.here.com" target="_blank">HERE platform</a>.

## Health check

### Build and test

| Master                      | Node version       | Status                                                                                                                                                                                         |
| :-------------------------- | :----------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Build/Test/Bundling/Typedoc | Node 16.13.2 (LTS) | <a href="https://app.travis-ci.com/heremaps/here-data-sdk-typescript" target="_blank"><img src="https://app.travis-ci.com/heremaps/here-data-sdk-typescript.svg?branch=master" alt="Build Status"></a> |

### Test coverage

| Platform | Status                                                                                                                                                                                                              |
| :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Linux    | <a href="https://codecov.io/gh/heremaps/here-data-sdk-typescript/" target="_blank"><img src="https://codecov.io/gh/heremaps/here-data-sdk-typescript/branch/master/graph/badge.svg" alt="Linux code coverage"/></a> |

## Why use

HERE Data SDK for TypeScript provides support for the core HERE platform use cases. The Data SDK is intended to save your time and effort on using HERE REST APIs. It provides a set of stable APIs that simplify complex platform operations and keeps up to date with the latest HERE REST API changes.

Data SDK for TypeScrypt is a modern, lightweight, and modular SDK with minimal dependencies targeted towards a wide range of hardware platforms from embedded devices to desktops.

This SDK lets you:

- Authenticate to the HERE platform using client credentials.
- Read catalog and partition metadata.
- Retrieve data from layers.
- Publish data to layers
- Delete data from an object store layer

Additionally, the Data SDK includes classes for work with geospatial tiling schemes that are used by most platform catalog layers.

## Backward compatibility

We try to develop and maintain our API in a way that preserves its compatibility with the existing applications. Changes in Data SDK for TypeScript are greatly influenced by the Data API development. Data API introduces breaking changes 6 months in advance. Therefore, you may need to migrate to a new version of Data SDK for TypeScript every half a year.

For more information on Data API, see its <a href="https://developer.here.com/documentation/data-api/data_dev_guide/index.html" target="_blank">Developer Guide</a> and <a href="https://developer.here.com/documentation/data-api/api-reference.html" target="_blank">API Reference</a>.

When new API is introduced in Data SDK for TypeScript, the old one is not deleted straight away. The standard API deprecation time is 6 months. It gives you time to switch to new code. However, we do not provide ABI backward compatibility.

All of the deprecated methods, functions, and parameters are documented in the Data SDK for TypeScript <a href="https://developer.here.com/documentation/sdk-typescript/api_reference/index.html"  target="_blank">API Reference</a> and <a href="https://github.com/heremaps/here-data-sdk-typescript/blob/master/CHANGELOG.md" target="_blank">changelog</a>.

For more information on Data SDK for TypeScrypt, see our <a href="https://developer.here.com/documentation/sdk-typescript/dev_guide/index.html" target="blank">Developer Guide</a>.

## About this repository

The Data SDK repository is a monorepo that contains the core components of the platform SDK organized in the NPM workspace.

All components can be used stand-alone and are in the <a href="https://github.com/heremaps/here-data-sdk-typescript/tree/master/%40here" target="_blank">@here</a> subdirectory.

## LICENSE

Copyright (C) 2019–2022 HERE Europe B.V.

For license details, see the <a href="https://github.com/heremaps/here-data-sdk-typescript/blob/master/LICENSE" target="_blank">LICENSE</a> file in the root of this project.
