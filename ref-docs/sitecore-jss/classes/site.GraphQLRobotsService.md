[@sitecore-jss/sitecore-jss](../README.md) / [site](../modules/site.md) / GraphQLRobotsService

# Class: GraphQLRobotsService

[site](../modules/site.md).GraphQLRobotsService

Service that fetch the robots.txt data using Sitecore's GraphQL API.

## Table of contents

### Constructors

- [constructor](site.GraphQLRobotsService.md#constructor)

### Properties

- [graphQLClient](site.GraphQLRobotsService.md#graphqlclient)
- [options](site.GraphQLRobotsService.md#options)

### Accessors

- [query](site.GraphQLRobotsService.md#query)

### Methods

- [fetchRobots](site.GraphQLRobotsService.md#fetchrobots)
- [getGraphQLClient](site.GraphQLRobotsService.md#getgraphqlclient)

## Constructors

### constructor

• **new GraphQLRobotsService**(`options`)

Creates an instance of graphQL robots.txt service with the provided options

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | [`GraphQLRobotsServiceConfig`](../modules/site.md#graphqlrobotsserviceconfig) | instance |

#### Defined in

[packages/sitecore-jss/src/site/graphql-robots-service.ts:48](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/site/graphql-robots-service.ts#L48)

## Properties

### graphQLClient

• `Private` **graphQLClient**: [`GraphQLClient`](../interfaces/index.GraphQLClient.md)

#### Defined in

[packages/sitecore-jss/src/site/graphql-robots-service.ts:38](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/site/graphql-robots-service.ts#L38)

___

### options

• **options**: [`GraphQLRobotsServiceConfig`](../modules/site.md#graphqlrobotsserviceconfig)

instance

#### Defined in

[packages/sitecore-jss/src/site/graphql-robots-service.ts:48](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/site/graphql-robots-service.ts#L48)

## Accessors

### query

• `Protected` `get` **query**(): `string`

#### Returns

`string`

#### Defined in

[packages/sitecore-jss/src/site/graphql-robots-service.ts:40](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/site/graphql-robots-service.ts#L40)

## Methods

### fetchRobots

▸ **fetchRobots**(): `Promise`\<`string`\>

Fetch a data of robots.txt from API

#### Returns

`Promise`\<`string`\>

text of robots.txt

**`Throws`**

if the siteName is empty.

#### Defined in

[packages/sitecore-jss/src/site/graphql-robots-service.ts:57](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/site/graphql-robots-service.ts#L57)

___

### getGraphQLClient

▸ `Protected` **getGraphQLClient**(): [`GraphQLClient`](../interfaces/index.GraphQLClient.md)

Gets a GraphQL client that can make requests to the API. Uses graphql-request as the default
library for fetching graphql data (@see GraphQLRequestClient). Override this method if you
want to use something else.

#### Returns

[`GraphQLClient`](../interfaces/index.GraphQLClient.md)

implementation

#### Defined in

[packages/sitecore-jss/src/site/graphql-robots-service.ts:82](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/site/graphql-robots-service.ts#L82)
