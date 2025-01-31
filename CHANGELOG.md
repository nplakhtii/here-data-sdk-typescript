## v1.12.2 (11/01/2022)

**olp-sdk-dataservice-read**

- `StreamLayerClient::poll()` now blocks sending a backend request if there are no messages to submit (https://github.com/heremaps/here-data-sdk-typescript/pull/495).
- `getTile` now does not throw an error on sparse versioned or volatile layers (https://github.com/heremaps/here-data-sdk-typescript/pull/496).
- Improved the interactive map layer API (https://github.com/heremaps/here-data-sdk-typescript/pull/497).

## v1.12.1 (16/09/2021)

**olp-sdk-dataservice-api**

- Updated the `value` parameter in the `UrlBuilder.appendQuery()` method. You can also use this parameter as an object: `{ [key: string]: string | number }`.
- Updated the APIs generated by the Interactive API v1. Some interfaces have breaking changes: https://github.com/heremaps/here-data-sdk-typescript/commit/70d7d8799de59c23157dc0437eef0f78a46c8b63.

## v1.12.0 (30/08/2021)

**olp-sdk-core**

- Updated the `@here/olp-sdk-dataservice-api` dependency.

**olp-sdk-authentication**

- Removed the deprecated code (https://github.com/heremaps/here-data-sdk-typescript/pull/485).
- Updated the `@here/olp-sdk-core` dependency.

**olp-sdk-dataservice-api**

- Updated the generated code for `ConfigAPI` with information on the `InteractiveMap` and `ObjectStore` layer types.
- Updated the `date` types for the `Schema`, `Artifact`, and `KeysListObjectItemResponse` interfaces of `ArtifactAPI`.
- Removed the deprecated code (https://github.com/heremaps/here-data-sdk-typescript/pull/485).

**olp-sdk-dataservice-read**

- Removed the deprecated code (https://github.com/heremaps/here-data-sdk-typescript/pull/485).
- Updated the `@here/olp-sdk-core` dependency.
- Updated the `@here/olp-sdk-dataservice-api` dependency.

**olp-sdk-dataservice-write**

- Updated the `@here/olp-sdk-core` dependency.
- Updated the `@here/olp-sdk-dataservice-api` dependency.

## v1.11.1 (17/06/2021)

**olp-sdk-dataservice-write**

- Disable type checking for line `import { fs } from "@here/olp-sdk-core";` in `NodeFileData` private class.

**olp-sdk-core**

- Change typings settings to `index.web`.

## v1.11.0 (07/06/2021)

**olp-sdk-dataservice-write**

- Updated dependencies.

**olp-sdk-dataservice-api**

- Added the APIs generated by the `Interactive V1` specification to support IML layers.

**olp-sdk-core**

- Updated dependencies.

**olp-sdk-authentication**

- Updated dependencies.

**olp-sdk-dataservice-read**

- Updated dependencies.

## v1.10.0 (14/05/2021)

**olp-sdk-dataservice-write**

- Added the `MultiPartUploadWrapper` class. You can use it to upload large files in a browser and Node.js to the Blob API v1 and v2 services in chunks.
- Changed `VersionedLayerClient`. Now, to upload large files to versioned layers, use the `MultiPartUploadWrapper` class.
- Added the abstracted `BlobData` class. It is a wrapper of data (`Blob`, `Buffer`, `File`, string, and so on)
  that allows to read a specific range of bytes and get data size.

**olp-sdk-dataservice-api**

- Fixed the issue with the incorrect `body` parameter in the `ObjectApi.startMultipartUploadByKey` function.

**olp-sdk-core**

- Added export for `fs` symbols to the Node.js index file.

**olp-sdk-authentication**

- Updated dependencies.

**olp-sdk-dataservice-read**

- Updated dependencies.

## v1.9.1 (24/03/2021)

**olp-sdk-dataservice-api**

- Fixed the bug related to the crash in the Config API that occurred when the `catalogExists` function was called.

## v1.9.0 (11/02/2021)

**olp-sdk-core**

- Added the `isValid` method to `TileKey`.
- Fixed the bug related to handling 202 and 303 responses.
- Extended the `HttpError` messages by adding details from the response if it exists.
- Changed the Lookup API host URL for SIT.
- Updated dependencies.

**olp-sdk-authentication**

- Removed the deprecated code (https://github.com/heremaps/here-data-sdk-typescript/pull/425).
- Updated dependencies.

**olp-sdk-fetch**

- Updated dependencies.

**olp-sdk-dataservice-api**

- Removed the deprecated code (https://github.com/heremaps/here-data-sdk-typescript/pull/425).
- Added the APIs generated by `Blob V2`.
- Updated dependencies.

**olp-sdk-dataservice-read**

- Removed the deprecated code (https://github.com/heremaps/here-data-sdk-typescript/pull/425).
- Updated dependencies.

**olp-sdk-dataservice-write**

- Updated dependencies.

## v1.8.0 (07/12/2020)

**olp-sdk-core**

- Changed the webpack configuration for bundling JS.

**olp-sdk-authentication**

- Added the maximum validity of the token `expiresIn` parameter to `UserAuthConfig`.
- Changed the webpack configuration for bundling JS.

**olp-sdk-fetch**

- Changed the webpack configuration for bundling JS.

**olp-sdk-dataservice-api**

- Changed the webpack configuration for bundling JS.

**olp-sdk-dataservice-read**

- Changed the webpack configuration for bundling JS.

**olp-sdk-dataservice-write**

- Changed the webpack configuration for bundling JS.

## v1.7.0 (02/11/2020)

**olp-sdk-core**

- Added the `sentWith` query parameter to each request.
- Updated dependencies.

**olp-sdk-authentication**

- Added the `sentWith` query parameter to each request.
- Updated dependencies.

**olp-sdk-fetch**

- Updated dependencies.

**olp-sdk-dataservice-api**

- Added generated functions and interfaces that support Authorization APIs. You can find them at `@here/olp-sdk-dataservice-api/lib/authorization-api-v1.1.ts`.
- Added the `Content-Encoding` header to the PUT blob request. Without this header, it was not possible to upload gzipped blobs.
- **Breaking change** Removed deprecated items that have exceeded the six-month deprecation period. @see [#385](https://github.com/heremaps/here-data-sdk-typescript/pull/385).
- Updated dependencies.

**olp-sdk-dataservice-read**

- Now, using a version in the `MetadataCacheRepository` request class is deprecated and will be removed by 05.2021.
- Updated dependencies.
- **Breaking change** Removed deprecated items that have exceeded the six-month deprecation period. @see [#385](https://github.com/heremaps/here-data-sdk-typescript/pull/385).

**olp-sdk-dataservice-write**

- Updated dependencies.

## v1.6.0 (21/09/2020)

**olp-sdk-core**

- Removed the `User-Agent` custom header from the requests. This was necessary due to issues sending a custom user-agent in Mozilla browsers.

**olp-sdk-authentication**

- Removed the `User-Agent` custom header from the requests. This was necessary due to issues sending a custom user-agent in Mozilla browsers.
- Updated `@here/olp-sdk-fetch` to version 1.6.0.

**olp-sdk-dataservice-api**

- Added generated functions and interfaces for supporting Authorization APIs. You can find them in `@here/olp-sdk-dataservice-api/lib/authorization-api-v1.1.ts`.

**olp-sdk-fetch**

- Updated dependencies.

**olp-sdk-dataservice-read**

- Fixed the issue with caching partitions metadata without additional fields.
- Started using `RequestFactory` from the `@here/olp-sdk-core` package.

**olp-sdk-dataservice-write**

- Added `@here/olp-sdk-dataservice-api` as a dependency.
- Updated `@here/olp-sdk-core` to version 1.1.0.
- Updated `@here/olp-sdk-fetch` to version 1.6.0.

## v1.5.1 (19/08/2020)

**olp-sdk-core**

- Added `@here/olp-sdk-dataservice-api` as a dependency.

**olp-sdk-authentication**

- Updated `olp-sdk-core` to version ^1.0.0.

**olp-sdk-dataservice-read**

- Updated `olp-sdk-core` to version ^1.0.0.

**olp-sdk-dataservice-write**

- Updated `olp-sdk-core` to version ^1.0.0.

## v1.5.0 (18/08/2020)

**olp-sdk-core**

- Added the new `@here/olp-sdk-core` module v1.0.0 and moved common components to it.

**olp-sdk-authentication**

- Added `@here/olp-sdk-core` as a dependency.
- Updated `olp-sdk-fetch` to version 1.5.0.
- Deprecated the `lib.version.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `./lib/HttpError.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.

**olp-sdk-dataservice-api**

- Added the `checkBlobExistsStatus` function to `blob-api.ts`. It is a fork of the `checkBlobExists` function.
- Deprecated the `checkBlobExists` function in `blob-api.ts`. It will be removed by 02.2021. Use the `checkBlobExistsStatus` function instead.
- Added the `doCompleteMultipartUpload` function to `blob-api.ts`. It is a fork of the `completeMultipartUpload` function.
- Deprecated the `completeMultipartUpload` function in `blob-api.ts`. It will be removed by 02.2021. Use the `doCompleteMultipartUpload` function instead.
- Added the `putData` function to `blob-api.ts`. It is a fork of the `putBlob` function.
- Deprecated the `putBlob` function in `blob-api.ts`. It will be removed by 02.2021. Use the `putData` function instead.
- Added the `doUploadPart` function to `blob-api.ts`. It is a fork of the `uploadPart` function.
- Deprecated the `uploadPart` function in `blob-api.ts`. It will be removed by 02.2021. Use the `doUploadPart` function instead.
- Deprecated the `./lib/HttpError.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead..

**olp-sdk-fetch**

- Updated dependencies.

**olp-sdk-dataservice-read**

- Added `@here/olp-sdk-core` as a dependency.
- Deprecated the `lib.version.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/DataStoreDownloadManager.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/DataStoreRequestBuilder.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/DownloadManager.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/HRN.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/ApiCacheRepository.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/KeyValueCache.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/LRUCache.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `DataRequest.getQuadKey` method. It will be removed by 02.2021. If you need to get data using a quadkey, use the [[getAggregatedData]] method instead.
- Deprecated the `lib/FetchOptions.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/OlpClientSettings.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/QuadKey.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/getEnvLookupUrl.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/getDataSizeUtil.ts` file. It will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `lib/utils/RequestBuilderFactory.ts` file. This file will be removed by 02.2021. Use the same from the `@here/olp-sdk-core` package instead.
- Deprecated the `TileRequestParams` parameter required to construct `TileRequest`. This signature will be removed by 02.2021. Use the new `TileRequest()` parameter instead.
- Deprecated the `TileRequest.getCatalogVersion()` method. It will be removed by 02.2021. Call the `getTile` method with the following signature instead: `getTile(request: TileRequest, params: TileRequestParams, abortSignal?: AbortSignal)`.
- Deprecated the signature for the following function: `getTile(request: TileRequest, abortSignal?: AbortSignal): Promise<Response>;`. This signature will be removed by 02.2021. Use the following signature instead: `getTile(request: TileRequest, params: TileRequestParams, abortSignal?: AbortSignal): Promise<Response>`.
- Added the `getAggregatedTile` method to `VersionedLayerClient` and `VolatileLayerClient`. This method fetches data of a tile or its closest ancestor. Use the `getAggregatedTile` method for tile-tree structures where children tile data is aggregated and stored in parent tiles.

**olp-sdk-dataservice-write**

- Added the new `olp-sdk-dataservice-write` module that you can use to upload data to catalogs. For instruction, see the [related](https://developer.here.com/documentation/sdk-typescript/dev_guide/topics/publish-data.html) section in the Developer Guide.
- Added `VersionedLayerClient`. You can use it to upload data to versioned layers.
- Added the `VersionedLayerClient.checkDataExists()` method. You can use it to check if a data handle is not used in a layer.
- Added the `VersionedLayerClient.getBaseVersion()` method. You can use it to get the latest version of a catalog.
- Added the `VersionedLayerClient.startBatch()` method. You can use it to initialize a new publication for publishing.
- Added the `VersionedLayerClient.publishToBatch()` method. You can use it to upload a blob and metadata of one partition. If you upload more than 50 MB of data, the data is split and uploaded in parts of 5 MB each.
- Added the `VersionedLayerClient.uploadBlob()` method. You can use it to upload data blobs of multiple partitions. If you upload more than 50 MB of data, the data is split and uploaded in parts of 5 MB each.
- Added the `VersionedLayerClient.uploadPartitions()` method. You can use it to upload metadata to the write service.
- Added the `VersionedLayerClient.cancelBatch()` method. You can use it to cancel a publication if it has not been submitted.
- Added the `VersionedLayerClient.getBatch()` method. You can use it to retrieve publication details.
- Added the `VersionedLayerClient.completeBatch()` method. You can use it to submit a publication, that is a batch, and if necessary, initiate post-processing.

## v1.4.0 (30/04/2020)

**olp-sdk-authentication**

- Updated `olp-sdk-fetch` to version 1.4.0.

**olp-sdk-dataservice-api**

- Deprecated the `commitOffsets` function in `stream-api.ts`. It will be removed by 09.2020. Use the `doCommitOffsets` function instead.

**olp-sdk-fetch**

- Updated dependencies.

**olp-sdk-dataservice-read**

- Added the `LRUCache` class.
- Replaced `Map` with `LRUCache` in `KeyValueCache`. The default LRU cache capacity is 2 MB.
- Added metadata caching to the `getPartitions` and `getData` methods in `VersionedLayerClient` and `VolatileLayerClient`.
- Added the `getSize`, `setCapacity`, and `getCapacity` methods to `KeyValueCache`. You can use these methods to perform the following actions with the LRU cache instance: retrieve the current size, set a new size, and retrieve the total capacity.
- Deprecated the `getQuadKey` and `withQuadKey` methods in `DataRequest`. Both methods will be removed by 10.2020. Use the `getTile` function instead.
- Added the `getTile` helper function for retrieving binary data of a versioned or volatile layer using a tile key. This function will optimize the metadata caching by requesting a quadtree with depth 4. This way, all the following requests within the same quadtree will benefit from the already cached metadata.
- Added the `withFetchOption` and `getFetchOption` methods to `DataRequest` and `PartitionsRequest`. You can use these methods to define how and from where to retrieve data and metadata. Possible options are `OnlineIfNotFound`, and `OnlineOnly`.
- Updated `olp-sdk-fetch` to version 1.4.0.

## v1.3.1 (11/03/2020)

**olp-sdk-dataservice-read**

- Fixed API breaks in `VersionedLayerClient` and `VolatileLayerClient`.
- Fixed the incorrectly handled version in `VersionedLayerClient`, `CatalogClient`, and `QueryClient`.
- Fixed the incorrectly handled headers in `DatastoreRequestBuilder`.

## v1.3.0 (05/03/2020)

**Common**

- Updated dependencies.

The following bugs are fixed:

- Version "0" was incorrectly handled. It is now fixed.
- Additional fields were not passed correctly into the request. It is now fixed.

**olp-sdk-fetch**

- Updated `node-fetch` to version 2.6.0.

**olp-sdk-authentication**

- Updated `olp-sdk-fetch` to version 1.3.0.

**olp-sdk-dataservice-api**

- Added functions and models that are generated from the Stream API specification.
- Added the `isHttpError()` method to the `HttpError` class.
- Changed `CoverageAPI`. Now, the `dataLevel` parameter is optional.

**olp-sdk-dataservice-read**

- Added the `VersionedLayerClientParams` interface.
- Deprecated the `VersionedLayerClient` constructor. Instead, use the constructor that creates the `VersionedLayerClient` instance with the help of the `VersionedLayerClientParams` object.
- Added the `VersionedLayerClient` constructor that creates the `VersionedLayerClient` instance using the `VersionedLayerClientParams` object and lock version.
- Deprecated the `DataRequest.getVersion()` method.
- Deprecated the `DataRequest.withVersion()` method.
- Changed the `VersionedLayerClient.getData` and `VersionedLayerClient.getPartitions` methods. Now, they ignore versions from `DataRequest` and `PartitionsRequest` and use versions from the `VersionedLayerClient` instance. If you initialize `VersionedLayerClient` without any version, on the first call, the latest version is fetched from the service and set in the instance.
- Added the `SubscribeRequest` class. This is used by `StreamLayerClient.subscribe()`.
- Deprecated the `StatisticsRequest.withDatalevel()` method with a string parameter and added the `StatisticsRequest.withDatalevel()` method with a number parameter.
- Changed `StatisticsRequest.getDataLevel()`. Now, it returns one of the following values: string, number, or undefined.
- Added `StreamLayerClient` and reading support for streamed data using `StreamLayerClient`. Currently, you can subscribe, unsubscribe, and consume messages from a stream layer in a serial or parallel mode. The `poll` method reads messages from a stream layer and commits successfully consumed messages before handing them over to you. With the `seek` method, you can set to start reading messages from a stream layer at any given position.
- Added the `PollRequest` class. It is used by `StreamLayerClient.poll()`.
- Added the `UnsubscribeRequest` class. It is used by `StreamLayerClient.unsubscribe()`.
- Added the `SeekRequest` class. It is used by `StreamLayerClient.seek()`.
- Deprecated the `VolatileLayerClient`constructor. Instead, use the constructor that creates the `VolatileLayerClient` instance with the help of the `VolatileLayerClientParams` object.
- Added the `VolatileLayerClient` constructor that creates the `VolatileLayerClient` instance using `VolatileLayerClientClientParams` object.
- Deprecated the `IndexLayerClient` constructor. Instead, use the constructor that creates the `IndexLayerClientClient` instance with the help of the `IndexLayerClientClientParams` object.
- Added the `IndexLayerClient` constructor that creates the `IndexLayerClientClient` instance using the `IndexLayerClientClientParams` object.
- Changed the `LookupAPI.getBaseUrl()` method. Now, you can fetch all URLs in one request instead of fetching each URL separately.
- Changed the `ConfigClient.getCatalogs()` method. Now, the `request` parameter is optional.

## v1.2.1 (05/02/2020)

**Common**

- Updated the development dependencies.

**olp-sdk-dataservice-read**

- Fixed the crash in `VersionedLayerClient` and `VolatileLayerClient` that happened when a non-existing tile was requested.

**olp-sdk-authentication**

- Reverted the API break in `AuthCredentials`.

## v1.2.0 (04/02/2020)

**Common**

- Updated the development dependencies.

**olp-sdk-dataservice-read**

- Added the `IndexLayerClient` class that is used to access index layers on OLP. This class implements the `getPartitions` and `getData` methods.
- Added the `HttpError` class that extends the `Error` class and adds a status code to HTTP errors.
- Improved error propagations in all public methods. Now, these methods reject the promises with the `HttpError` instance or `Error` class when errors occur.

**olp-sdk-authentication**

- Added the `HttpError` class that extends the `Error` class and adds a status code to HTTP errors.
- Improved error propagations in all public methods. Now, these methods reject the promises with the `HttpError` instance or `Error` class when errors occur.

- **Breaking Change** Improved the return type of the `getEarliestVersion` method in `CatalogClient`. It is now the same as the return type of the `getLatestVersion` method.
- **Breaking Change** Public methods now reject the promises with the `HttpError` instance or `Error` class instead of strings when errors occur.

## v1.1.0 (11/12/2019)

**Common**

- Updated the development dependencies.

**olp-sdk-dataservice-read**

- Added the `getPartitionsById` method to `QueryClient`. Now, you can fetch metadata from specific partitions using their IDs.
- Updated the `getPartitions` method in `VersionedLayerClient` and `VolatileLayerClient`. Now, you can fetch metadata from specific partitions of a volatile or versioned layer using partitions IDs.
- Updated documentation for the public API.

**olp-sdk-authentication**

- The scope support was added to `UserAuth` through `UserAuthConfig`. You can now access the project bound resources using the `UserAuthConfig` scope field.
- Updated documentation for the public API.

## v1.0.0 (02/12/2019)

**olp-sdk-dataservice-read**

- Added new class `OlpClientSetting` with `KeyValueCache` instance to be used for context.
- Added the `VersionedLayerClient` class that is used to access versioned layers on OLP. This class implements the `getData` and `getPartitions` methods.
- Added the `VolatileLayerClient` class that is used to access volatile layers on OLP. This class implements the `getPartitions` and `getData` methods.
- Added the `ArtifactClient` class that is used to access the artifact service on OLP. This class implements the `getSchemaDetails` and `getSchema` methods.
- Added the `ConfigClient` class that is used to access the configuration service on OLP. This class implements the `getCatalogs` method.
- Added the `QueryClient` class that is used to access the query service on OLP. This class implements the `fetchQuadTreeIndex` method.
- Added a possibility to abort requests using `AbortSignal`.
- Added a possibility to set an optional billing tag in each request.
- Added `QuadKeyUtils` that has a set of utilities and functions intended for work with quadkeys: convert a quadkey to a Morton code, convert a Morton code to a quadkey, and validate a quadkey.
- Added the `RequestFactory` class that is used for look-up requests. This class implements the static `create` method that returns the built `DatastoreDownloadManager` instance with a correct base URL to service, and the `getBaseUrl` method that caches and returns base URLs to services.
- The `CatalogClient` constructor changed. Users must pass now `OlpClientSettings` by value not by reference anymore. Removed `KeyValueCache` as it is now a part of `OlpClientSettings`.

- **Breaking Change** The `getLayer` method was removed from `CatalogClient`. Now, to initialize a deprecated `CatalogLayer`, use the `VersionedLayerClient` or `VolatileLayerClient` classes.
- **Breaking Change** The `getTile` method was removed from `CatalogClient`. Now, to get layer data, use `VersionedLayerClient.getData()` or `VolatileLayerClient.getData()`.
- **Breaking Change** The `getAgregatedTile` method was removed from `CatalogClient`. Now, to get partitions metadata and layer data, use `VersionedLayerClient.getPartitions()` and `VersionedLayerClient.getData()` or `VolatileLayerClient.getPartitions()` and `VolatileLayerClient.getData()`.
- **Breaking Change** The `getSchema` and `getSchemaDetails` methods were removed from `CatalogClient`. Now, to get schemas and schema metadata, use the `ArtifactClient` class.
- **Breaking Change** The `HypeDataProvider` class was removed. Now, catalog and layer clients can be initialized without additional classes.
- **Breaking Change** The `DatastoreClient` class was removed. Now, `CatalogClient` can be initialized without additional classes.
- **Breaking Change** Replaced RequestInit with AbortSignal in all public APIs.

**olp-sdk-dataservice-api**

- Fixed issues with requests to the Blob REST APIs.

**olp-sdk-authentication**

- Added a possibility to read credentials from a file using Node.js.

## v0.9.2-beta (28/10/2019)

- Changed prepare process before publishing.
- Changed configuration to the TypeDoc.
- Fixed tslints.
- Align Version and Volatile Layers with DatastoreApi.

## v0.9.1-beta (17/10/2019)

**olp-sdk-authentication**

- Fixed build process for web.
- **Breaking Change** UserAuthConfig.tokenRequester is required now.

**olp-sdk-dataservice-read**

- Fixed build process for web.
