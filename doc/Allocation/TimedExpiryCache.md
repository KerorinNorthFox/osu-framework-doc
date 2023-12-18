- [Class TimedExpiryCache\<TKey, TValue\> #](#class-timedexpirycachetkey-tvalue-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
  - [Properties](#properties)
    - [DisposeOnRemoval](#disposeonremoval)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [ExpiryTime](#expirytime)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
    - [CheckPeriod](#checkperiod)
      - [Declaration](#declaration-3)
      - [Type](#type-2)
  - [Methods](#methods)
    - [Add](#add)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments)
    - [TryGetValue](#trygetvalue)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-1)
      - [Type](#type-3)
    - [Dispose](#dispose)
      - [Declaration](#declaration-6)
      - [Arguments](#arguments-2)
    - [Dispose](#dispose-1)
      - [Declaration](#declaration-7)



# Class TimedExpiryCache\<TKey, TValue\> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/TimedExpiryCache.cs#L15)
指定された有効期限後のアイテムのクリーンアップをサポートするキーと値のストア。


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()


## Syntax
```csharp
public class TimedExpiryCache<TKey, TValue> : IDisposable
```


## Constructor
#### Declaration
```csharp
public TimedExpiryCache()
```


## Properties

### DisposeOnRemoval
[IDisposable]()項目を削除時に破棄するかどうか。
#### Declaration
```csharp
public bool DisposeOnRemoval = true;
```
#### Type
|Type|Description|
|:-|:-|
|bool||

### ExpiryTime
最後にアクセスしてから項目がクリーンアップされるまでの時間 (ミリ秒)。
#### Declaration
```csharp
public int ExpiryTime = 5000;
```
#### Type
|Type|Description|
|:-|:-|
|int||

### CheckPeriod
有効期限をチェックする間隔 (ミリ秒単位)。
#### Declaration
```csharp
public readonly int CheckPeriod = 5000;
```
#### Type
|Type|Description|
|:-|:-|
|int||


## Methods

### Add
#### Declaration
```csharp
public void Add(TKey key, TValue value)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`key`|TKey||
|`value`|TValue||

### TryGetValue
#### Declaration
```csharp
public bool TryGetValue(TKey key, out TValue value)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`key`|TKey||
|`value`|TValue||
#### Type
|Type|Description|
|:-|:-|
|bool||

### Dispose
#### Declaration
```csharp
protected virtual void Dispose(bool disposing)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`disposing`|bool||

### Dispose
#### Declaration
```csharp
public void Dispose()
```