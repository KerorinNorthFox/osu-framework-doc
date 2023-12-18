- [Interface IReadOnlyDependencyContainer #](#interface-ireadonlydependencycontainer-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Methods](#methods)
    - [Get](#get)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Return](#return)
    - [Get](#get-1)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
      - [Return](#return-1)
    - [Inject\<T\>](#injectt)
      - [Type](#type)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-2)
- [Class ReadOnlyDependencyContainerExtensions #](#class-readonlydependencycontainerextensions-)
  - [Namespace](#namespace-1)
  - [Syntax](#syntax-1)
  - [Methods](#methods-1)
    - [Get\<T\>](#gett)
      - [Type](#type-1)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-3)
      - [Return](#return-2)
    - [Get\<T\>](#gett-1)
      - [Type](#type-2)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-4)
      - [Return](#return-3)
    - [TryGet\<T\>](#trygett)
      - [Type](#type-3)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-5)
      - [Return](#return-4)
    - [TryGet\<T\>](#trygett-1)
      - [Type](#type-4)
      - [Declaration](#declaration-6)
      - [Arguments](#arguments-6)
      - [Return](#return-5)



# Interface IReadOnlyDependencyContainer [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IReadOnlyDependencyContainer.cs#L14)
型に基づいて依存関係を注入および取得できる依存関係コンテナへの読み取り専用インターフェース。


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public interface IReadOnlyDependencyContainer
```


## Methods

### Get
`type`のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。
#### Declaration
```csharp
object Get(Type type);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|クエリする依存関係のタイプ|
#### Return
|Type|Description|
|:-|:-|
|object|要求された依存関係。見つからない場合は null。|

### Get
`type`のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。
#### Declaration
```csharp
object Get(Type type, CacheInfo info);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|クエリする依存関係のタイプ|
|`info`|[CacheInfo]()|キャッシュされた依存関係を識別する追加情報。|
#### Return
|Type|Description|
|:-|:-|
|object|要求された依存関係。見つからない場合は null。|

### Inject\<T\>
指定されたインスタンスに依存関係を注入する。
#### Type
|Type|Description|
|:-|:-|
|T|依存関係を注入するインスタンスのタイプ。|
#### Declaration
```csharp
void Inject<T>(T instance) where T : class, IDependencyInjectionCandidate;
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`instance`|T|依存関係を注入するインスタンス。|



---
# Class ReadOnlyDependencyContainerExtensions [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IReadOnlyDependencyContainer.cs#L39)


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public static class ReadOnlyDependencyContainerExtensions
```


## Methods

### Get\<T\>
`T`型のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。
#### Type
|Type|Description|
|:-|:-|
|T|クエリする依存関係のタイプ。|
#### Declaration
```csharp
public static T Get<T>(this IReadOnlyDependencyContainer container)
    where T : class
    => Get<T>(container, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`container`|[IReadOnlyDependencyContainer]()|クエリする[IReadOnlyDependencyContainer]()|
#### Return
|Type|Description|
|:-|:-|
|T|要求された依存関係。見つからない場合は null。|

### Get\<T\>
`T`型のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。
#### Type
|Type|Description|
|:-|:-|
|T|クエリする依存関係のタイプ。|
#### Declaration
```csharp
public static T Get<T>(this IReadOnlyDependencyContainer container, CacheInfo info)
    where T : class
    => (T)container.Get(typeof(T), info);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`container`|[IReadOnlyDependencyContainer]()|クエリする[IReadOnlyDependencyContainer]()|
|`info`|[CacheInfo]()|キャッシュされた依存関係を識別する追加情報。|
#### Return
|Type|Description|
|:-|:-|
|T|要求された依存関係。見つからない場合は null。|

### TryGet\<T\>
`T`型のキャッシュされた依存関係の取得を試みる。
#### Type
|Type|Description|
|:-|:-|
|T|クエリする依存関係のタイプ。|
#### Declaration
```csharp
public static bool TryGet<T>(this IReadOnlyDependencyContainer container, out T value)
    where T : class
    => TryGet(container, out value, default);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`container`|[IReadOnlyDependencyContainer]()|クエリする[IReadOnlyDependencyContainer]()|
|`value`|T|要求された依存関係。見つからない場合は null。|
#### Return
|Type|Description|
|:-|:-|
|bool|要求された依存関係が存在するかどうか。|

### TryGet\<T\>
`T`型のキャッシュされた依存関係の取得を試みる。
#### Type
|Type|Description|
|:-|:-|
|T|クエリする依存関係のタイプ。|
#### Declaration
```csharp
public static bool TryGet<T>(this IReadOnlyDependencyContainer container, out T value, CacheInfo info)
    where T : class
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`container`|[IReadOnlyDependencyContainer]()|クエリする[IReadOnlyDependencyContainer]()|
|`value`|T|要求された依存関係。見つからない場合は null。|
|`info`|[CacheInfo]()|キャッシュされた依存関係を識別する追加情報。|
#### Return
|Type|Description|
|:-|:-|
|bool|要求された依存関係が存在するかどうか。|