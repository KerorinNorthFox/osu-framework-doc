- [Class ResolvedAttribute #](#class-resolvedattribute-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments)
  - [Properties](#properties)
    - [Parent](#parent)
      - [Declaration](#declaration-2)
      - [Type](#type)
    - [Name](#name)
      - [Declaration](#declaration-3)
      - [Type](#type-1)
    - [CanBeNull](#canbenull)
      - [Declaration](#declaration-4)
      - [Type](#type-2)
- [Class PropertyNotWritableException #](#class-propertynotwritableexception-)
  - [Namespace](#namespace-1)
  - [Implements](#implements-1)
  - [Syntax](#syntax-1)
  - [Constructor](#constructor-1)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-1)



# Class ResolvedAttribute [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ResolvedAttribute.cs#L28)
[Drawable]()コンポーネントのプロパティに付加され、プロパティの値を依存関係キャッシュから取得する必要があることを示す属性。<br>
この属性でマークされたプロパティはプライベートであり、セッターを持っている必要がある。<br>
プロパティの値は、ターゲット[Drawable]()の[Drawable.Load]()で解決されます。


## Namespace
osu.Framework.Allocation


## Implements
[Attribute]()


## Syntax
```csharp
[MeansImplicitUse(ImplicitUseKindFlags.Assign)]
[AttributeUsage(AttributeTargets.Property)]
public class ResolvedAttribute : Attribute
```


## Constructor
[DependencyContainer]()から解決されるメンバーを識別する。
#### Declaration
```csharp
public ResolvedAttribute()
```

---
#### Declaration
```csharp
public ResolvedAttribute(Type parent = null, string name = null, bool canBeNull = false)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`parent` = null|[Type]()||
|`name` = null|string||
|`canBeNull` = false|bool||


## Properties

### Parent
[DependencyContainer]()内のキャッシュされたメンバーの包含タイプ。<br>
これは、メンバーがカスタム[CacheInfo]()でキャッシュされた場合にのみ設定される。
#### Declaration
```csharp
public Type Parent;
```
#### Type
|Type|Description|
|:-|:-|
|[Type]()||

### Name
[DependencyContainer]()内のキャッシュされたメンバーの名前。<br>
これは、メンバーがカスタム[CacheInfo]()でキャッシュされた場合にのみ設定される。
#### Declaration
```csharp
public string Name;
```
#### Type
|Type|Description|
|:-|:-|
|string||

### CanBeNull
メンバーがキャッシュに存在しない場合に null 値を受け入れることができるかどうか。
#### Declaration
```csharp
public bool CanBeNull;
```
#### Type
|Type|Description|
|:-|:-|
|bool||



---
# Class PropertyNotWritableException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ResolvedAttribute.cs#L121)


## Namespace
osu.Framework.Allocation


## Implements
[Exception]()


## Syntax
```csharp
public class PropertyNotWritableException : Exception
```


## Constructor
#### Declaration
```csharp
public PropertyNotWritableException(Type type, string propertyName)
    : base($"Attempting to inject dependencies into non-write-able property {propertyName} of type {type.ReadableName()}.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()||
|`propertyName`|string||