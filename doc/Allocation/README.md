# osu.Framework.Allocation Doc
- [osu.Framework.Allocation Doc](#osuframeworkallocation-doc)
- [インターフェース](#インターフェース)
  - [`IDependencyActivatorRegistry` #](#idependencyactivatorregistry-)
  - [`IDependencyInjectionCandidate` #](#idependencyinjectioncandidate-)
  - [`IReadOnlyDependencyContainer` #](#ireadonlydependencycontainer-)
  - [`ISourceGeneratedDependencyActivator` #](#isourcegenerateddependencyactivator-)
  - [`ISourceGeneratedLongRunningLoadCache` #](#isourcegeneratedlongrunningloadcache-)
- [クラス](#クラス)
  - [`BackgroundDependencyLoaderAttribute` #](#backgrounddependencyloaderattribute-)
  - [`CachedAttribute` #](#cachedattribute-)
  - [`NullDependencyException` #](#nulldependencyexception-)
  - [`CachedModelDependencyContainer<TModel>` #](#cachedmodeldependencycontainertmodel-)
  - [`MultipleDependencyLoaderMethodsException` #](#multipledependencyloadermethodsexception-)
  - [`DependencyNotRegisteredException` #](#dependencynotregisteredexception-)
  - [`AccessModifierNotAllowedForMemberException` #](#accessmodifiernotallowedformemberexception-)
  - [`AccessModifierNotAllowedForCachedValueException` #](#accessmodifiernotallowedforcachedvalueexception-)
  - [`AccessModifierNotAllowedForLoaderMethodException` #](#accessmodifiernotallowedforloadermethodexception-)
  - [`AccessModifierNotAllowedForPropertySetterException` #](#accessmodifiernotallowedforpropertysetterexception-)
  - [`DependencyContainer` #](#dependencycontainer-)
  - [`TypeAlreadyCachedException` #](#typealreadycachedexception-)
  - [`ReadOnlyDependencyContainerExtensions` #](#readonlydependencycontainerextensions-)
  - [`InvokeOnDisposal` #](#invokeondisposal-)
  - [`InvokeOnDisposal<T>` #](#invokeondisposalt-)
  - [`LongRunningLoadAttribute` #](#longrunningloadattribute-)
  - [`ObjectUsage<T>` #](#objectusaget-)
  - [`ResolvedAttribute` #](#resolvedattribute-)
  - [`PropertyNotWritableException` #](#propertynotwritableexception-)
  - [`TimedExpiryCache<TKey, TValue>` #](#timedexpirycachetkey-tvalue-)
  - [`TripleBuffer<T>` #](#triplebuffert-)
- [構造体](#構造体)
  - [`CacheInfo` #](#cacheinfo-)
  - [`ObjectHandle<T>` #](#objecthandlet-)
  - [`ValueInvokeOnDisposal` #](#valueinvokeondisposal-)
  - [`ValueInvokeOnDisposal<T>` #](#valueinvokeondisposalt-)
- [列挙型](#列挙型)
  - [`UsageType` #](#usagetype-)
- [デリゲート](#デリゲート)
  - [`InjectDependencyDelegate` #](#injectdependencydelegate-)
  - [`CacheDependencyDelegate` #](#cachedependencydelegate-)



# インターフェース
## `IDependencyActivatorRegistry` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IDependencyActivator.cs#L11)
```csharp
public interface IDependencyActivatorRegistry
```

## `IDependencyInjectionCandidate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IDependencyInjectionCandidate.cs#L9)
```csharp
public interface IDependencyInjectionCandidate
```

## `IReadOnlyDependencyContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IReadOnlyDependencyContainer.cs#L14)
```csharp
public interface IReadOnlyDependencyContainer
```

## `ISourceGeneratedDependencyActivator` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ISourceGeneratedDependencyActivator.cs#L12)
```csharp
public interface ISourceGeneratedDependencyActivator
```

## `ISourceGeneratedLongRunningLoadCache` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ISourceGeneratedLongRunningLoadCache.cs#L8)
```csharp
public interface ISourceGeneratedLongRunningLoadCache
```



# クラス
## `BackgroundDependencyLoaderAttribute` [#](./BackgroundDependencyLoaderAttribute.md)
メソッドを[Graphics.Drawable]()の (非同期の可能性がある) 初期化メソッドとしてマークし、メソッドのパラメーターを介して依存関係を自動的に挿入できるようにする。
```csharp
public class BackgroundDependencyLoaderAttribute : Attribute
```

## `CachedAttribute` [#](./CachedAttribute.md)
```csharp
public class CachedAttribute : Attribute
```

## `NullDependencyException` [#](./CachedAttribute.md#class-nulldependencyexception)
```csharp
public sealed class NullDependencyException : InvalidOperationException
```

## `CachedModelDependencyContainer<TModel>` [#](./CachedModelDependencyContainer.md)
`TModel`とそれに含まれるメンバーを依存関係として[CachedAttribute]()でアタッチしてキャッシュする[DependencyContainer]()。<br>
ユーザーは、`TModel`型を直接クエリしてモデルをクエリしたり、[TModel]()型を親として指定してモデルの依存関係をクエリしたりする。
```csharp
public class CachedModelDependencyContainer<TModel> : IReadOnlyDependencyContainer
        where TModel : class, IDependencyInjectionCandidate, new()
```

## `MultipleDependencyLoaderMethodsException` [#](./DependencyActivator.md#class-multipledependencyloadermethodsexception)
1 つのオブジェクトに複数の[BackgroundDependencyLoaderAttribute]()が存在する場合に発生する。
```csharp
public class MultipleDependencyLoaderMethodsException : Exception
```

## `DependencyNotRegisteredException` [#](./DependencyActivator.md#class-dependencynotregisteredexception)
```csharp
public class DependencyNotRegisteredException : Exception
```
オブジェクトが依存関係の解決を要求したが、依存関係が存在しない場合に発生する。<br>
これは、親[CompositeDrawable]()から[CompositeDrawable.CreateChildDependency]()または[CachedAttribute]()によって依存関係が登録されていないことが原因で発生する。

## `AccessModifierNotAllowedForMemberException` [#](./DependencyActivator.md#accessmodifiernotallowedformemberexception)
許容できないアクセス修飾子を持つメンバーに対して依存関係に関連した操作が発生したときに発生する。
```csharp
public abstract class AccessModifierNotAllowedForMemberException : InvalidOperationException
```

## `AccessModifierNotAllowedForCachedValueException` [#](./DependencyActivator.md#class-accessmodifiernotallowedforcachedvalueexception)
[CachedAttribute]()が添付された非プライベートおよび非読み取り専用フィールドをキャッシュしようとしたときに発生する。
```csharp
public class AccessModifierNotAllowedForCachedValueException : AccessModifierNotAllowedForMemberException
```

## `AccessModifierNotAllowedForLoaderMethodException` [#](./DependencyActivator.md#class-accessmodifiernotallowedforloadermethodexception)
[BackgroundDependencyLoaderAttribute]()が添付されたメソッドがプライベートではない場合に発生する。
```csharp
public class AccessModifierNotAllowedForLoaderMethodException : AccessModifierNotAllowedForMemberException
```

## `AccessModifierNotAllowedForPropertySetterException` [#](./DependencyActivator.md#class-accessmodifiernotallowedforpropertysetterexception)
[ResolvedAttribute]()が添付されたプロパティのセッターがプライベートではない場合に発生する。
```csharp
public class AccessModifierNotAllowedForPropertySetterException : AccessModifierNotAllowedForMemberException
```

## `DependencyContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyContainer.cs#L16)
```csharp
public class DependencyContainer : IReadOnlyDependencyContainer
```

## `TypeAlreadyCachedException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyContainer.cs#L191)
```csharp
public class TypeAlreadyCachedException : InvalidOperationException
```

## `ReadOnlyDependencyContainerExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IReadOnlyDependencyContainer.cs#L39)
```csharp
public static class ReadOnlyDependencyContainerExtensions
```

## `InvokeOnDisposal` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/InvokeOnDisposal.cs#L16)
```csharp
public class InvokeOnDisposal : IDisposable
```

## `InvokeOnDisposal<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/InvokeOnDisposal.cs#L51)
```csharp
public class InvokeOnDisposal<T> : IDisposable
```

## `LongRunningLoadAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/LongRunningLoadAttribute.cs#L17)
```csharp
public class LongRunningLoadAttribute : Attribute
```

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
## `CacheInfo` [#](./CacheInfo.md)
```csharp
public readonly struct CacheInfo : IEquatable<CacheInfo>
```

## `ObjectHandle<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ObjectHandle.cs#L14)
```csharp
public struct ObjectHandle<T> : IDisposable
```

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
## `InjectDependencyDelegate` [#](./DependencyActivator.md#delegate-injectdependencydelegate)
```csharp
public delegate void InjectDependencyDelegate(object target, IReadOnlyDependencyContainer dependencies);
```

## `CacheDependencyDelegate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L223)
```csharp
public delegate IReadOnlyDependencyContainer CacheDependencyDelegate(object target, IReadOnlyDependencyContainer existingDependencies, CacheInfo info);
```