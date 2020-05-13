[@speechly/browser-client](../README.md) › ["index.d"](_index_d_.md)

# Module: "index.d"

## Index

### References

* [Storage](_index_d_.md#storage)

### Enumerations

* [ClientState](../enums/_index_d_.clientstate.md)
* [WebsocketResponseType](../enums/_index_d_.websocketresponsetype.md)

### Classes

* [Client](../classes/_index_d_.client.md)

### Interfaces

* [APIClient](../interfaces/_index_d_.apiclient.md)
* [ClientOptions](../interfaces/_index_d_.clientoptions.md)
* [Entity](../interfaces/_index_d_.entity.md)
* [EntityResponse](../interfaces/_index_d_.entityresponse.md)
* [Intent](../interfaces/_index_d_.intent.md)
* [IntentResponse](../interfaces/_index_d_.intentresponse.md)
* [Microphone](../interfaces/_index_d_.microphone.md)
* [Segment](../interfaces/_index_d_.segment.md)
* [TentativeEntitiesResponse](../interfaces/_index_d_.tentativeentitiesresponse.md)
* [TentativeTranscriptResponse](../interfaces/_index_d_.tentativetranscriptresponse.md)
* [TranscriptResponse](../interfaces/_index_d_.transcriptresponse.md)
* [WebsocketResponse](../interfaces/_index_d_.websocketresponse.md)
* [Word](../interfaces/_index_d_.word.md)

### Type aliases

* [AudioCallback](_index_d_.md#audiocallback)
* [CloseCallback](_index_d_.md#closecallback)
* [EntityCallback](_index_d_.md#entitycallback)
* [IntentCallback](_index_d_.md#intentcallback)
* [ResponseCallback](_index_d_.md#responsecallback)
* [SegmentChangeCallback](_index_d_.md#segmentchangecallback)
* [StateChangeCallback](_index_d_.md#statechangecallback)
* [TentativeEntitiesCallback](_index_d_.md#tentativeentitiescallback)
* [TentativeTranscriptCallback](_index_d_.md#tentativetranscriptcallback)
* [TranscriptCallback](_index_d_.md#transcriptcallback)

### Variables

* [DefaultSampleRate](_index_d_.md#const-defaultsamplerate)
* [ErrAlreadyInitialized](_index_d_.md#const-erralreadyinitialized)
* [ErrDeviceNotSupported](_index_d_.md#const-errdevicenotsupported)
* [ErrKeyNotFound](_index_d_.md#const-errkeynotfound)
* [ErrNoAudioConsent](_index_d_.md#const-errnoaudioconsent)
* [ErrNoStorageSupport](_index_d_.md#const-errnostoragesupport)
* [ErrNotInitialized](_index_d_.md#const-errnotinitialized)

### Functions

* [stateToString](_index_d_.md#statetostring)

## References

###  Storage

• **Storage**:

## Type aliases

###  AudioCallback

Ƭ **AudioCallback**: *function*

Defined in index.d.ts:64

A callback that receives an ArrayBuffer representing a frame of audio.

#### Type declaration:

▸ (`audioBuffer`: ArrayBuffer): *void*

**Parameters:**

Name | Type |
------ | ------ |
`audioBuffer` | ArrayBuffer |

___

###  CloseCallback

Ƭ **CloseCallback**: *function*

Defined in index.d.ts:235

A callback that is invoked whenever WebSocket connection is closed.

#### Type declaration:

▸ (`err`: Error): *void*

**Parameters:**

Name | Type |
------ | ------ |
`err` | Error |

___

###  EntityCallback

Ƭ **EntityCallback**: *function*

Defined in index.d.ts:274

A callback that is invoked whenever new entity is received from the API.

#### Type declaration:

▸ (`contextId`: string, `segmentId`: number, `entity`: [Entity](../interfaces/_index_d_.entity.md)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`contextId` | string |
`segmentId` | number |
`entity` | [Entity](../interfaces/_index_d_.entity.md) |

___

###  IntentCallback

Ƭ **IntentCallback**: *function*

Defined in index.d.ts:356

A callback that is invoked whenever new intent (tentative or not) is received from the API.

#### Type declaration:

▸ (`contextId`: string, `segmentId`: number, `intent`: [Intent](../interfaces/_index_d_.intent.md)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`contextId` | string |
`segmentId` | number |
`intent` | [Intent](../interfaces/_index_d_.intent.md) |

___

###  ResponseCallback

Ƭ **ResponseCallback**: *function*

Defined in index.d.ts:410

A callback that is invoked whenever a response is received from Speechly SLU WebSocket API.

#### Type declaration:

▸ (`response`: [WebsocketResponse](../interfaces/_index_d_.websocketresponse.md)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`response` | [WebsocketResponse](../interfaces/_index_d_.websocketresponse.md) |

___

###  SegmentChangeCallback

Ƭ **SegmentChangeCallback**: *function*

Defined in index.d.ts:447

A callback that is invoked whenever current {@link Segment | segment} changes.

#### Type declaration:

▸ (`segment`: [Segment](../interfaces/_index_d_.segment.md)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`segment` | [Segment](../interfaces/_index_d_.segment.md) |

___

###  StateChangeCallback

Ƭ **StateChangeCallback**: *function*

Defined in index.d.ts:453

A callback that is invoked whenever the {@link ClientState | client state} changes.

#### Type declaration:

▸ (`state`: [ClientState](../enums/_index_d_.clientstate.md)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`state` | [ClientState](../enums/_index_d_.clientstate.md) |

___

###  TentativeEntitiesCallback

Ƭ **TentativeEntitiesCallback**: *function*

Defined in index.d.ts:510

A callback that is invoked whenever new tentative entities are received from the API.

#### Type declaration:

▸ (`contextId`: string, `segmentId`: number, `entities`: [Entity](../interfaces/_index_d_.entity.md)[]): *void*

**Parameters:**

Name | Type |
------ | ------ |
`contextId` | string |
`segmentId` | number |
`entities` | [Entity](../interfaces/_index_d_.entity.md)[] |

___

###  TentativeTranscriptCallback

Ƭ **TentativeTranscriptCallback**: *function*

Defined in index.d.ts:527

A callback that is invoked whenever a new tentative transcript is received from the API.

#### Type declaration:

▸ (`contextId`: string, `segmentId`: number, `words`: [Word](../interfaces/_index_d_.word.md)[], `text`: string): *void*

**Parameters:**

Name | Type |
------ | ------ |
`contextId` | string |
`segmentId` | number |
`words` | [Word](../interfaces/_index_d_.word.md)[] |
`text` | string |

___

###  TranscriptCallback

Ƭ **TranscriptCallback**: *function*

Defined in index.d.ts:548

A callback that is invoked whenever a new transcript is received from the API.

#### Type declaration:

▸ (`contextId`: string, `segmentId`: number, `word`: [Word](../interfaces/_index_d_.word.md)): *void*

**Parameters:**

Name | Type |
------ | ------ |
`contextId` | string |
`segmentId` | number |
`word` | [Word](../interfaces/_index_d_.word.md) |

## Variables

### `Const` DefaultSampleRate

• **DefaultSampleRate**: *16000* = 16000

Defined in index.d.ts:241

Default sample rate for microphone streams.

___

### `Const` ErrAlreadyInitialized

• **ErrAlreadyInitialized**: *Error*

Defined in index.d.ts:305

Error to be thrown when the initialize method of a Microphone instance is called more than once.

___

### `Const` ErrDeviceNotSupported

• **ErrDeviceNotSupported**: *Error*

Defined in index.d.ts:311

Error to be thrown when the device does not support the Microphone instance's target audio APIs.

___

### `Const` ErrKeyNotFound

• **ErrKeyNotFound**: *Error*

Defined in index.d.ts:317

Error to be thrown if requested key was not found in the storage.

___

### `Const` ErrNoAudioConsent

• **ErrNoAudioConsent**: *Error*

Defined in index.d.ts:323

Error to be thrown when user did not give consent to the application to record audio.

___

### `Const` ErrNoStorageSupport

• **ErrNoStorageSupport**: *Error*

Defined in index.d.ts:329

Error to be thrown if storage API is not supported by the device.

___

### `Const` ErrNotInitialized

• **ErrNotInitialized**: *Error*

Defined in index.d.ts:335

Error to be thrown when the microphone was accessed before it was initialized.

## Functions

###  stateToString

▸ **stateToString**(`state`: [ClientState](../enums/_index_d_.clientstate.md)): *string*

Defined in index.d.ts:460

Converts client state value to a string, which could be useful for debugging or metrics.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`state` | [ClientState](../enums/_index_d_.clientstate.md) | the state of the client |

**Returns:** *string*
