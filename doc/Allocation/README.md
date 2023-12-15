# osu.Framework.Allocation Doc
- [osu.Framework.Allocation Doc](#osuframeworkallocation-doc)
- [インターフェース](#インターフェース)
  - [`IDependencyActivatorRegistry` #](#idependencyactivatorregistry-)
  - [`IDependencyInjectionCandidate` #](#idependencyinjectioncandidate-)
  - [`IReadOnlyDependencyContainer` #](#ireadonlydependencycontainer-)
  - [`ISourceGeneratedDependencyActivator` #](#isourcegenerateddependencyactivator-)
  - [`ISourceGeneratedLongRunningLoadCache` #](#isourcegeneratedlongrunningloadcache-)
- [Class](#class)
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


# Class
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

## `CachedModelDependencyContainer<TModel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/CachedModelDependencyContainer.cs#L21)
```csharp
public class CachedModelDependencyContainer<TModel> : IReadOnlyDependencyContainer
        where TModel : class, IDependencyInjectionCandidate, new()
```

## `MultipleDependencyLoaderMethodsException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L154)
```csharp
public class MultipleDependencyLoaderMethodsException : Exception
```

## `DependencyNotRegisteredException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L168)
```csharp
public class DependencyNotRegisteredException : Exception
```

## `AccessModifierNotAllowedForMemberException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L179)
```csharp
public abstract class AccessModifierNotAllowedForMemberException : InvalidOperationException
```

## `AccessModifierNotAllowedForCachedValueException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L190)
```csharp
public class AccessModifierNotAllowedForCachedValueException : AccessModifierNotAllowedForMemberException
```

## `AccessModifierNotAllowedForLoaderMethodException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L202)
```csharp
public class AccessModifierNotAllowedForLoaderMethodException : AccessModifierNotAllowedForMemberException
```

## `AccessModifierNotAllowedForPropertySetterException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L213)
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
## `InjectDependencyDelegate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L221)
```csharp
public delegate void InjectDependencyDelegate(object target, IReadOnlyDependencyContainer dependencies);
```

## `CacheDependencyDelegate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L223)
```csharp
public delegate IReadOnlyDependencyContainer CacheDependencyDelegate(object target, IReadOnlyDependencyContainer existingDependencies, CacheInfo info);
```