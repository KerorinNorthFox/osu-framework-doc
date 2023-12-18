- [Class ObjectUsage\<T\> #](#class-objectusaget-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Properties](#properties)
    - [Object](#object)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [Usage](#usage)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
    - [Index](#index)
      - [Declaration](#declaration-3)
      - [Type](#type-2)
  - [Methods](#methods)
    - [Dispose](#dispose)
      - [Declaration](#declaration-4)
- [Enum UsageType #](#enum-usagetype-)
  - [Namespace](#namespace-1)
  - [Declaration](#declaration-5)



# Class ObjectUsage\<T\> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ObjectUsage.cs#L8)


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()


## Syntax
```csharp
public class ObjectUsage<T> : IDisposable
    where T : class
```


## Constructor
#### Declaration
```csharp
public ObjectUsage(int index, Action<ObjectUsage<T>>? finish)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`index`|int||
|`finish`|[Action]()\<[ObjectUsage]()\<T\>\>||


## Properties

### Object
#### Declaration
```csharp
public T? Object;
```
#### Type
|Type|Description|
|:-|:-|
|T||

### Usage
この使用法がアクティブに書き込まれているか、または読み取られているかどうか。
#### Declaration
```csharp
public UsageType Usage;
```
#### Type
|Type|Description|
|:-|:-|
|[UsageType]()||

### Index
#### Declaration
```csharp
public readonly int Index;
```
#### Type
|Type|Description|
|:-|:-|
|int||


## Methods

### Dispose
#### Declaration
```csharp
public void Dispose()
```



---
# Enum UsageType [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ObjectUsage.cs#L34)


## Namespace
osu.Framework.Allocation


## Declaration
```csharp
public enum UsageType
{
    None,
    Read,
    Write
}
```