- [Class TripleBuffer\<T\> #](#class-triplebuffert-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
  - [Methods](#methods)
    - [GetForWrite](#getforwrite)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [GetForRead](#getforread)
      - [Declaration](#declaration-2)
      - [Type](#type-1)



# Class TripleBuffer\<T\> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/TripleBuffer.cs#L16)
あらゆる種類のオブジェクトのトリプルバッファリングを処理する。<br>
スレッドセーフティでは、最大1人の書き込み者と1人の読み取り者が想定される。<br>
最新の[GetForRead]()オブジェクトが書き込まれていないことがさらに保証される。


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public class TripleBuffer<T>
    where T : class
```


## Constructor
#### Declaration
```csharp
public TripleBuffer()
```


## Methods

### GetForWrite
#### Declaration
```csharp
public ObjectUsage<T> GetForWrite()
```
#### Type
|Type|Description|
|:-|:-|
|[ObjectUsage\<T\>]()||

### GetForRead
#### Declaration
```csharp
public ObjectUsage<T>? GetForRead()
```
#### Type
|Type|Description|
|:-|:-|
|[ObjectUsage\<T\>]()||