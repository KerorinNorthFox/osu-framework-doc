- [Class DependencyContainer #](#class-dependencycontainer-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Methods](#methods)
    - [Cache](#cache)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
    - [Cache](#cache-1)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-2)
    - [CacheAs\<T\>](#cacheast)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-3)
    - [CacheAs\<T\>](#cacheast-1)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-4)
    - [CacheAs\<T\>](#cacheast-2)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-5)
    - [CacheAs\<T\>](#cacheast-3)
      - [Declaration](#declaration-6)
      - [Arguments](#arguments-6)
    - [Get](#get)
      - [Declaration](#declaration-7)
      - [Arguments](#arguments-7)
      - [Return](#return)
    - [Get](#get-1)
      - [Declaration](#declaration-8)
      - [Arguments](#arguments-8)
      - [Return](#return-1)
    - [Inject\<T\>](#injectt)
      - [Type](#type)
      - [Declaration](#declaration-9)
      - [Arguments](#arguments-9)
        - [Exception](#exception)
- [Class TypeAlreadyCachedException #](#class-typealreadycachedexception-)
  - [Namespace](#namespace-1)
  - [Implements](#implements-1)
  - [Syntax](#syntax-1)
  - [Constructor](#constructor-1)
      - [Declaration](#declaration-10)
      - [Arguments](#arguments-10)



# Class DependencyContainer [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyContainer.cs#L16)
依存関係を階層的にキャッシュし、依存関係注入用に登録された型に依存関係を自動的に注入できる。


## Namespace
osu.Framework.Allocation


## Implements
[IReadOnlyDependencyContainer]()


## Syntax
```csharp
public class DependencyContainer : IReadOnlyDependencyContainer
```


## Constructor
新しいDependencyContainerインスタンスを作成する。
#### Declaration
```csharp
public DependencyContainer(IReadOnlyDependencyContainer parent = null)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`parent` = null|[IReadOnlyDependencyContainer]()|キャッシュルックアップのフォールバックとして使用するオプションの親コンテナ。|


## Methods

### Cache
型のインスタンスをその最も派生した型としてキャッシュする。このインスタンスは、
[Get(Type)]()するたびに返される。
#### Declaration
```csharp
public void Cache(object instance)
    => Cache(instance, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`instance`|object|キャッシュするインスタンス。|

### Cache
型のインスタンスをその最も派生した型としてキャッシュする。このインスタンスは、
[Get(Type)]()するたびに返される。
#### Declaration
```csharp
public void Cache(object instance, CacheInfo info)
    => CacheAs(instance.GetType(), info, instance, false);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`instance`|object|キャッシュするインスタンス。|
|`info`|[CacheInfo]()|キャッシュ内の`instance`を識別するための追加情報。|

### CacheAs\<T\>
型のインスタンスを`T`の型としてキャッシュする。このインスタンスは、[Get(Type)]()するたびに返される。
#### Declaration
```csharp
public void CacheAs<T>(T instance) where T : class
    => CacheAs(instance, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`instance`|object|キャッシュするインスタンス。`T`であるか、`T`から派生する必要がある。|

### CacheAs\<T\>
型のインスタンスを`T`の型としてキャッシュする。このインスタンスは、[Get(Type)]()するたびに返される。
#### Declaration
```csharp
public void CacheAs<T>(T instance, CacheInfo info) where T : class
    => CacheAs(typeof(T), info, instance, false);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`instance`|object|キャッシュするインスタンス。`T`であるか、`T`から派生する必要がある。|
|`info`|[CacheInfo]()|キャッシュ内の`instance`を識別するための追加情報。|

### CacheAs\<T\>
型のインスタンスを`type`の型としてキャッシュする。このインスタンスは、[Get(Type)]()するたびに返される。
#### Declaration
```csharp
public void CacheAs<T>(Type type, T instance) where T : class
    => CacheAs(type, instance, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|`instance`としてキャッシュするタイプ。|
|`instance`|object|キャッシュするインスタンス。`type`であるか、`type`から派生する必要がある。|

### CacheAs\<T\>
型のインスタンスを`type`の型としてキャッシュする。このインスタンスは、[Get(Type)]()するたびに返される。
#### Declaration
```csharp
public void CacheAs<T>(Type type, T instance, CacheInfo info) where T : class
    => CacheAs(type, info, instance, false);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|`instance`としてキャッシュするタイプ。|
|`instance`|object|キャッシュするインスタンス。`type`であるか、`type`から派生する必要がある。|
|`info`|[CacheInfo]()|キャッシュ内の`instance`を識別するための追加情報。|

### Get
#### Declaration
```csharp
public object Get(Type type)
    => Get(type, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()||
#### Return
|Type|Description|
|:-|:-|
|object||

### Get
#### Declaration
```csharp
public object Get(Type type, CacheInfo info)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()||
|`info`|[CacheInfo]()||
#### Return
|Type|Description|
|:-|:-|
|object||

### Inject\<T\>
指定されたインスタンスに依存関係を注入する。
#### Type
|Type|Description|
|:-|:-|
|T|依存関係を注入するインスタンスのタイプ。|
#### Declaration
```csharp
public void Inject<T>(T instance)
    where T : class, IDependencyInjectionCandidate
    => DependencyActivator.Activate(instance, this);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`instance`|T|依存関係を注入するインスタンス。|
##### Exception
|Name|Description|
|:-|:-|
|[OperationCanceledException]()|依存関係を注入するインスタンス。|



---
# Class TypeAlreadyCachedException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyContainer.cs#L191)


## Namespace
osu.Framework.Allocation


## Implements
[InvalidOperationException]()


## Syntax
```csharp
public class TypeAlreadyCachedException : InvalidOperationException
```


## Constructor
#### Declaration
```csharp
public TypeAlreadyCachedException(CacheInfo info)
    : base($"An instance of the member ({info.ToString()}) has already been cached to the dependency container.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`info`|[CacheInfo]()||