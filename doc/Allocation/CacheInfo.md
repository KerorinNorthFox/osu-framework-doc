- [Struct CacheInfo #](#struct-cacheinfo-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Fields](#fields)
    - [Name](#name)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [Parent](#parent)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
  - [Methods](#methods)
    - [ToString](#tostring)
      - [Declaration](#declaration-3)
      - [Return](#return)
    - [Equals](#equals)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-1)
      - [Return](#return-1)
    - [Equals](#equals-1)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-2)
      - [Return](#return-2)
    - [GetHashCode](#gethashcode)
      - [Declaration](#declaration-6)
      - [Return](#return-3)


# Struct CacheInfo [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/CacheInfo.cs#L11)


## Namespace
osu.Framework.Allocation


## Implements
[IEquatable\<CacheInfo\>]()


## Syntax
```csharp
public readonly struct CacheInfo : IEquatable<CacheInfo>
```


## Constructor
#### Declaration
```csharp
public CacheInfo(string name = null, Type parent = null)
    : this(null, name, parent)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`name` = null|string||
|`parent` = null|[Type]()||


## Fields

### Name
キャッシュされたメンバーの名前。
#### Declaration
```csharp
public readonly string Name;
```
#### Type
|Type|Description|
|:-|:-|
|string||

---
### Parent
キャッシュされたメンバーを含むタイプ。
#### Declaration
```csharp
public readonly Type Parent;
```
#### Type
|Type|Description|
|:-|:-|
|[Type]()|


## Methods

### ToString
#### Declaration
```csharp
public override string ToString() => $"{nameof(Type)} = {Type?.ReadableName()}, {nameof(Name)} = {Name}, {nameof(Parent)} = {Parent?.ReadableName()}";
```
#### Return
|Type|Description|
|:-|:-|
|string||

---
### Equals
#### Declaration
```csharp
public override bool Equals(object obj) => obj is CacheInfo cacheInfo && Equals(cacheInfo);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`obj`|object||
#### Return
|Type|Description|
|:-|:-|
|bool||

---
### Equals
#### Declaration
```csharp
public bool Equals(CacheInfo other) => Name == other.Name && Parent == other.Parent && Type == other.Type;
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`other`|[CacheInfo]()||
#### Return
|Type|Description|
|:-|:-|
|bool||

---
### GetHashCode
#### Declaration
```csharp
public override int GetHashCode() => HashCode.Combine(Name, Parent, Type);
```
#### Return
|Type|Description|
|:-|:-|
|int||