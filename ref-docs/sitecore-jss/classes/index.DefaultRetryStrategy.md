[@sitecore-jss/sitecore-jss](../README.md) / [index](../modules/index.md) / DefaultRetryStrategy

# Class: DefaultRetryStrategy

[index](../modules/index.md).DefaultRetryStrategy

Represents a default retry strategy for handling retry attempts in case of specific HTTP status codes.
This class implements the RetryStrategy interface and provides methods to determine whether a request
should be retried and calculates the delay before the next retry attempt.

## Implements

- [`RetryStrategy`](../interfaces/index.RetryStrategy.md)

## Table of contents

### Constructors

- [constructor](index.DefaultRetryStrategy.md#constructor)

### Properties

- [errorCodes](index.DefaultRetryStrategy.md#errorcodes)
- [factor](index.DefaultRetryStrategy.md#factor)
- [statusCodes](index.DefaultRetryStrategy.md#statuscodes)

### Methods

- [getDelay](index.DefaultRetryStrategy.md#getdelay)
- [shouldRetry](index.DefaultRetryStrategy.md#shouldretry)

## Constructors

### constructor

• **new DefaultRetryStrategy**(`options?`)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options` | `Object` | Configurable options for retry mechanism. |
| `options.errorCodes?` | `string`[] | Node error codes to trigger retries. Default is ['ECONNRESET', 'ETIMEDOUT', 'EPROTO']. |
| `options.factor?` | `number` | Factor by which the delay increases with each retry attempt. Default is 2. |
| `options.statusCodes?` | `number`[] | HTTP status codes to trigger retries on. Default is [429]. |

#### Defined in

[packages/sitecore-jss/src/graphql-request-client.ts:129](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/graphql-request-client.ts#L129)

## Properties

### errorCodes

• `Private` **errorCodes**: `string`[]

#### Defined in

[packages/sitecore-jss/src/graphql-request-client.ts:120](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/graphql-request-client.ts#L120)

___

### factor

• `Private` **factor**: `number`

#### Defined in

[packages/sitecore-jss/src/graphql-request-client.ts:121](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/graphql-request-client.ts#L121)

___

### statusCodes

• `Private` **statusCodes**: `number`[]

#### Defined in

[packages/sitecore-jss/src/graphql-request-client.ts:119](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/graphql-request-client.ts#L119)

## Methods

### getDelay

▸ **getDelay**(`error`, `attempt`): `number`

Calculates the delay (in milliseconds) before the next retry based on the given error and attempt count.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | [`GraphQLClientError`](../modules/graphql.md#graphqlclienterror) | The error received from the GraphQL request. |
| `attempt` | `number` | The current attempt number. |

#### Returns

`number`

The delay in milliseconds before the next retry.

#### Implementation of

[RetryStrategy](../interfaces/index.RetryStrategy.md).[getDelay](../interfaces/index.RetryStrategy.md#getdelay)

#### Defined in

[packages/sitecore-jss/src/graphql-request-client.ts:142](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/graphql-request-client.ts#L142)

___

### shouldRetry

▸ **shouldRetry**(`error`, `attempt`, `retries`): `boolean`

Determines whether a request should be retried based on the given error and attempt count.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `error` | [`GraphQLClientError`](../modules/graphql.md#graphqlclienterror) | The error received from the GraphQL request. |
| `attempt` | `number` | The current attempt number. |
| `retries` | `number` | The number of retries configured. |

#### Returns

`boolean`

A boolean indicating whether to retry the request.

#### Implementation of

[RetryStrategy](../interfaces/index.RetryStrategy.md).[shouldRetry](../interfaces/index.RetryStrategy.md#shouldretry)

#### Defined in

[packages/sitecore-jss/src/graphql-request-client.ts:135](https://github.com/Sitecore/jss/blob/577f1eaa2/packages/sitecore-jss/src/graphql-request-client.ts#L135)
