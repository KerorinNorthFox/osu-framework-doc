- [Class CachedModelDependencyContainer #](#class-cachedmodeldependencycontainer-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
      - [Type](#type)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Declaration](#declaration-1)
  - [Properties](#properties)
    - [Model](#model)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
  - [Methods](#methods)
    - [Get](#get)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-1)
      - [Return](#return)
    - [Get](#get-1)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-2)
      - [Return](#return-1)
    - [Inject\<T\>](#injectt)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-3)


# Class CachedModelDependencyContainer<TModel> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/CachedModelDependencyContainer.cs#L21)
`TModel`とそれに含まれるメンバーを依存関係として[CachedAttribute]()でアタッチしてキャッシュする[DependencyContainer]()。<br>
ユーザーは、`TModel`型を直接クエリしてモデルをクエリしたり、[TModel]()型を親として指定してモデルの依存関係をクエリしたりする。


## Namespace
osu.Framework.Allocation


## Implements
[IReadOnlyDependencyContainer]()


## Syntax
```csharp
public class CachedModelDependencyContainer<TModel> : IReadOnlyDependencyContainer
        where TModel : class, IDependencyInjectionCandidate, new()
```
#### Type
|Type|Description|
|:-|:-|
|TModel|キャッシュするモデルのタイプ。[Bindable\<T\>]()フィールドまたは自動プロパティのみを含める必要がある。|


## Constructor
#### Declaration
```csharp
public CachedModelDependencyContainer(IReadOnlyDependencyContainer parent)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`parent`|[IReadOnlyDependencyContainer]()||

---
#### Declaration
```csharp
static CachedModelDependencyContainer()
```


## Properties

### Model
キャッシュされた値を提供する`TModel`<br>
このモデルは直接挿入されません。[CachedModelDependencyContainer\<TModel\>]()のユーザーは、常にこの値のシャドウ バインドされたコピーを受け取る。
#### Declaration
```csharp
public readonly Bindable<TModel> Model = new Bindable<TModel>();
```
#### Type
|Type|Description|
|:-|:-|
|[Bindable\<TModel\>]()||


## Methods

### Get
#### Declaration
```csharp
public object Get(Type type) => Get(type, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|type|[Type]()||
#### Return
|Type|Description|
|:-|:-|
|object||

---
### Get
#### Declaration
```csharp
public object Get(Type type, CacheInfo info)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|type|[Type]()||
|info|[CacheInfo]()||
#### Return
|Type|Description|
|:-|:-|
|object||

---
### Inject\<T\>
#### Declaration
```csharp
public void Inject<T>(T instance)
    where T : class, IDependencyInjectionCandidate
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|instance|T||