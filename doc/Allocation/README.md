# osu.Framework.Allocation Doc
- [osu.Framework.Allocation Doc](#osuframeworkallocation-doc)
- [インターフェース](#インターフェース)
- [クラス](#クラス)
  - [`ObjectUsage<T>` #](#objectusaget-)
  - [`ResolvedAttribute` #](#resolvedattribute-)
  - [`PropertyNotWritableException` #](#propertynotwritableexception-)
  - [`TimedExpiryCache<TKey, TValue>` #](#timedexpirycachetkey-tvalue-)
  - [`TripleBuffer<T>` #](#triplebuffert-)
- [構造体](#構造体)
  - [`ValueInvokeOnDisposal` #](#valueinvokeondisposal-)
  - [`ValueInvokeOnDisposal<T>` #](#valueinvokeondisposalt-)
- [列挙型](#列挙型)
  - [`UsageType` #](#usagetype-)
- [デリゲート](#デリゲート)



# インターフェース
|Name|link|Description|
|:-|:-|:-|
|`IDependencyActivatorRegistry`|[link](./IDependencyActivator.md)|依存関係アクティブ化関数を登録するためのオブジェクトのインターフェース。|
|`IDependencyInjectionCandidate`|[link](./IDependencyInjectionCandidate.md)|[DependencyContainer.Inject\<T\>]()でオブジェクトを使用できるようにするためにオブジェクトにアタッチされるインターフェース。|
|`IReadOnlyDependencyContainer`|[link](./IReadOnlyDependencyContainer.md)|型に基づいて依存関係を注入および取得できる依存関係コンテナへの読み取り専用インターフェース。|
|`ISourceGeneratedDependencyActivator`|[link](./ISourceGeneratedDependencyActivator.md)|依存関係をオブジェクトに注入するためにソース ジェネレーターによって実装される。|
|`ISourceGeneratedLongRunningLoadCache`|[link](./ISourceGeneratedLongRunningLoadCache.md)||





# クラス
|Name|Link|Description|
|:-|:-|:-|
|`BackgroundDependencyLoaderAttribute`|[link](./BackgroundDependencyLoaderAttribute.md)|メソッドを[Graphics.Drawable]()の (非同期の可能性がある) 初期化メソッドとしてマークし、メソッドのパラメーターを介して依存関係を自動的に挿入できるようにする。|
|`CachedAttribute`|[link](./CachedAttribute.md)|[Drawable]()のクラス、インターフェイス、フィールド、またはプロパティ定義に添付して、値を依存関係としてキャッシュする必要があることを示す属性。<br>キャッシュされた値は、[BackgroundDependencyLoaderAttribute]()または[ResolvedAttribute]()を通じて解決できる。|
|`NullDependencyException`|[link](./CachedAttribute.md#class-nulldependencyexception)||
|`CachedModelDependencyContainer<TModel>`|[link](./CachedModelDependencyContainer.md)|`TModel`とそれに含まれるメンバーを依存関係として[CachedAttribute]()でアタッチしてキャッシュする[DependencyContainer]()。|
|`MultipleDependencyLoaderMethodsException`|[link](./DependencyActivator.md#class-multipledependencyloadermethodsexception)|1 つのオブジェクトに複数の[BackgroundDependencyLoaderAttribute]()が存在する場合に発生する。|
|`DependencyNotRegisteredException`|[link](./DependencyActivator.md#class-dependencynotregisteredexception)|オブジェクトが依存関係の解決を要求したが、依存関係が存在しない場合に発生する。<br>これは、親[CompositeDrawable]()から[CompositeDrawable.CreateChildDependency]()または[CachedAttribute]()によって依存関係が登録されていないことが原因で発生する。|
|`AccessModifierNotAllowedForMemberException`|[link](./DependencyActivator.md#accessmodifiernotallowedformemberexception)|許容できないアクセス修飾子を持つメンバーに対して依存関係に関連した操作が発生したときに発生する。|
|`AccessModifierNotAllowedForCachedValueException`|[link](./DependencyActivator.md#class-accessmodifiernotallowedforcachedvalueexception)|[CachedAttribute]()が添付された非プライベートおよび非読み取り専用フィールドをキャッシュしようとしたときに発生する。|
|`AccessModifierNotAllowedForLoaderMethodException`|[link](./DependencyActivator.md#class-accessmodifiernotallowedforloadermethodexception)|[BackgroundDependencyLoaderAttribute]()が添付されたメソッドがプライベートではない場合に発生する。|
|`AccessModifierNotAllowedForPropertySetterException`|[link](./DependencyActivator.md#class-accessmodifiernotallowedforpropertysetterexception)|[ResolvedAttribute]()が添付されたプロパティのセッターがプライベートではない場合に発生する。|
|`DependencyContainer`|[link](./DependencyContainer.md)|依存関係を階層的にキャッシュし、依存関係注入用に登録された型に依存関係を自動的に注入できる。|
|`TypeAlreadyCachedException`|[link](./DependencyContainer.md#class-typealreadycachedexception)||
|`ReadOnlyDependencyContainerExtensions`|[link](./IReadOnlyDependencyContainer.md#class-readonlydependencycontainerextensions)||
|`InvokeOnDisposal`|[link](./InvokeOnDisposal.md)|このクラスのインスタンスは、後のクリーンアップのためにアクションをキャプチャする。|
|`InvokeOnDisposal<T>`|[link](./InvokeOnDisposal.md)|このクラスのインスタンスは、後のクリーンアップのためにアクションをキャプチャする。|
|`LongRunningLoadAttribute`|[link](./LongRunningLoadAttribute.md)|[BackgroundDependencyLoaderAttribute]()メソッドで CPU を集中的に使用しない長時間実行タスクを実行するコンポーネントを示す。<br>長時間実行されるタスクは、優先度の低いスレッド プールにスケジュールされる。|






## `ObjectUsage<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ObjectUsage.cs#L8)
```csharp
public class ObjectUsage<T> : IDisposable
```

## `ResolvedAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ResolvedAttribute.cs#L28)
```csharp
[MeansImplicitUse(ImplicitUseKindFlags.Assign)]
[AttributeUsage(AttributeTargets.Property)]
public class ResolvedAttribute : Attribute
```

## `PropertyNotWritableException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ResolvedAttribute.cs#L121)
```csharp
public class PropertyNotWritableException : Exception
```

## `TimedExpiryCache<TKey, TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/TimedExpiryCache.cs#L15)
```csharp
public class TimedExpiryCache<TKey, TValue> : IDisposable
```

## `TripleBuffer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/TripleBuffer.cs#L16)
```csharp
public class TripleBuffer<T>
        where T : class
```



# 構造体
|Name|link|Description|
|:-|:-|:-|
|`CacheInfo`|[link](./CacheInfo.md)||
|`ObjectHandle<T>`|[link](./ObjectHandle.md)||




## `ValueInvokeOnDisposal` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ValueInvokeOnDisposal.cs#L18)
```csharp
public readonly struct ValueInvokeOnDisposal : IDisposable
```

## `ValueInvokeOnDisposal<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ValueInvokeOnDisposal.cs#L55)
```csharp
public readonly struct ValueInvokeOnDisposal<T> : IDisposable
```



# 列挙型
## `UsageType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ObjectUsage.cs#L34)
```csharp
public enum UsageType
```



# デリゲート
|Name|Link|Description|
|:-|:-|:-|
|`InjectDependencyDelegate`|[link](./DependencyActivator.md#delegate-injectdependencydelegate)||
|`CacheDependencyDelegate`|[link](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L223)||