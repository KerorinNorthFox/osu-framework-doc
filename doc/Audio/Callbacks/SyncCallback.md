- [Class SyncCallback #](#class-synccallback-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Properties](#properties)
    - [Callback](#callback)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [Sync](#sync)
      - [Declaration](#declaration-2)
      - [Type](#type-1)



# Class SyncCallback [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/SyncCallback.cs#L15)
[SyncProcedure]()のラッパーで、[BassCallback]()の機能を提供する。


## Namespace
osu.Framework.Audio.Callbacks


## Implements
[BassCallback]()


## Syntax
```csharp
public class SyncCallback : BassCallback
```


## Constructor
#### Declaration
```csharp
public SyncCallback(SyncProcedure proc)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`proc`|[SyncProcedure]()||


## Properties

### Callback
#### Declaration
```csharp
public SyncProcedure Callback => RuntimeFeature.IsDynamicCodeSupported ? Sync : syncCallback;
```
#### Type
|Type|Description|
|:-|:-|
|[SyncProcedure]()||

### Sync
#### Declaration
```csharp
public readonly SyncProcedure Sync;
```
#### Type
|Type|Description|
|:-|:-|
|[SyncProcedure]()||