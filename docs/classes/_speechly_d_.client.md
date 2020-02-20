[@speechly/browser-client](../README.md) › ["speechly.d"](../modules/_speechly_d_.md) › [Client](_speechly_d_.client.md)

# Class: Client

A client for Speechly Spoken Language Understanding (SLU) API. The client handles initializing the microphone
and websocket connection to Speechly API, passing control events and audio stream to the API, reading the responses
and dispatching them, as well as providing a high-level API for interacting with so-called speech segments.

## Hierarchy

* **Client**

## Index

### Constructors

* [constructor](_speechly_d_.client.md#constructor)

### Methods

* [close](_speechly_d_.client.md#close)
* [initialize](_speechly_d_.client.md#initialize)
* [onEntity](_speechly_d_.client.md#onentity)
* [onIntent](_speechly_d_.client.md#onintent)
* [onSegmentChange](_speechly_d_.client.md#onsegmentchange)
* [onStateChange](_speechly_d_.client.md#onstatechange)
* [onTentativeEntities](_speechly_d_.client.md#ontentativeentities)
* [onTentativeIntent](_speechly_d_.client.md#ontentativeintent)
* [onTentativeTranscript](_speechly_d_.client.md#ontentativetranscript)
* [onTranscript](_speechly_d_.client.md#ontranscript)
* [startContext](_speechly_d_.client.md#startcontext)
* [stopContext](_speechly_d_.client.md#stopcontext)

## Constructors

###  constructor

\+ **new Client**(`options`: [ClientOptions](../interfaces/_speechly_d_.clientoptions.md)): *[Client](_speechly_d_.client.md)*

Defined in speechly.d.ts:23

**Parameters:**

Name | Type |
------ | ------ |
`options` | [ClientOptions](../interfaces/_speechly_d_.clientoptions.md) |

**Returns:** *[Client](_speechly_d_.client.md)*

## Methods

###  close

▸ **close**(`cb?`: [ErrorCallback](../modules/_speechly_d_.md#errorcallback)): *void*

Defined in speechly.d.ts:34

Closes the client by closing the API connection and disabling the microphone.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb?` | [ErrorCallback](../modules/_speechly_d_.md#errorcallback) | the callback which is invoked when closure is complete.  |

**Returns:** *void*

___

###  initialize

▸ **initialize**(`cb?`: [ErrorCallback](../modules/_speechly_d_.md#errorcallback)): *void*

Defined in speechly.d.ts:29

Initializes the client, by initializing the microphone and establishing connection to the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb?` | [ErrorCallback](../modules/_speechly_d_.md#errorcallback) | the callback which is invoked when the initialization is complete.  |

**Returns:** *void*

___

###  onEntity

▸ **onEntity**(`cb`: [EntityCallback](../modules/_speechly_d_.md#entitycallback)): *void*

Defined in speechly.d.ts:74

Adds a listener for entity responses from the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [EntityCallback](../modules/_speechly_d_.md#entitycallback) | the callback to invoke on an entity response.  |

**Returns:** *void*

___

###  onIntent

▸ **onIntent**(`cb`: [IntentCallback](../modules/_speechly_d_.md#intentcallback)): *void*

Defined in speechly.d.ts:84

Adds a listener for intent responses from the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [IntentCallback](../modules/_speechly_d_.md#intentcallback) | the callback to invoke on an intent response.  |

**Returns:** *void*

___

###  onSegmentChange

▸ **onSegmentChange**(`cb`: [SegmentChangeCallback](../modules/_speechly_d_.md#segmentchangecallback)): *void*

Defined in speechly.d.ts:54

Adds a listener for current segment change events.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [SegmentChangeCallback](../modules/_speechly_d_.md#segmentchangecallback) | the callback to invoke on segment change events.  |

**Returns:** *void*

___

###  onStateChange

▸ **onStateChange**(`cb`: [StateChangeCallback](../modules/_speechly_d_.md#statechangecallback)): *void*

Defined in speechly.d.ts:49

Adds a listener for client state change events.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [StateChangeCallback](../modules/_speechly_d_.md#statechangecallback) | the callback to invoke on state change events.  |

**Returns:** *void*

___

###  onTentativeEntities

▸ **onTentativeEntities**(`cb`: [TentativeEntitiesCallback](../modules/_speechly_d_.md#tentativeentitiescallback)): *void*

Defined in speechly.d.ts:69

Adds a listener for tentative entities responses from the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [TentativeEntitiesCallback](../modules/_speechly_d_.md#tentativeentitiescallback) | the callback to invoke on a tentative entities response.  |

**Returns:** *void*

___

###  onTentativeIntent

▸ **onTentativeIntent**(`cb`: [IntentCallback](../modules/_speechly_d_.md#intentcallback)): *void*

Defined in speechly.d.ts:79

Adds a listener for tentative intent responses from the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [IntentCallback](../modules/_speechly_d_.md#intentcallback) | the callback to invoke on a tentative intent response.  |

**Returns:** *void*

___

###  onTentativeTranscript

▸ **onTentativeTranscript**(`cb`: [TentativeTranscriptCallback](../modules/_speechly_d_.md#tentativetranscriptcallback)): *void*

Defined in speechly.d.ts:59

Adds a listener for tentative transcript responses from the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [TentativeTranscriptCallback](../modules/_speechly_d_.md#tentativetranscriptcallback) | the callback to invoke on a tentative transcript response.  |

**Returns:** *void*

___

###  onTranscript

▸ **onTranscript**(`cb`: [TranscriptCallback](../modules/_speechly_d_.md#transcriptcallback)): *void*

Defined in speechly.d.ts:64

Adds a listener for transcript responses from the API.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb` | [TranscriptCallback](../modules/_speechly_d_.md#transcriptcallback) | the callback to invoke on a transcript response.  |

**Returns:** *void*

___

###  startContext

▸ **startContext**(`cb?`: [ContextCallback](../modules/_speechly_d_.md#contextcallback)): *void*

Defined in speechly.d.ts:39

Starts a new SLU context by sending a start context event to the API and unmuting the microphone.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb?` | [ContextCallback](../modules/_speechly_d_.md#contextcallback) | the callback which is invoked when the context start was acknowledged by the API.  |

**Returns:** *void*

___

###  stopContext

▸ **stopContext**(`cb?`: [ContextCallback](../modules/_speechly_d_.md#contextcallback)): *void*

Defined in speechly.d.ts:44

Stops current SLU context by sending a stop context event to the API and muting the microphone.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`cb?` | [ContextCallback](../modules/_speechly_d_.md#contextcallback) | the callback which is invoked when the context stop was acknowledged by the API.  |

**Returns:** *void*
