# osu.Framework.Allocation Doc
- [osu.Framework.Allocation Doc](#osuframeworkallocation-doc)
- [インターフェース](#インターフェース)
- [クラス](#クラス)
- [構造体](#構造体)
- [列挙型](#列挙型)
- [デリゲート](#デリゲート)



# インターフェース
|Name|link|Description|
|:-|:-|:-|
|`IDependencyActivatorRegistry`|[link](./IDependencyActivator.md)||
|`IDependencyInjectionCandidate`|[link](./IDependencyInjectionCandidate.md)||
|`IReadOnlyDependencyContainer`|[link](./IReadOnlyDependencyContainer.md)||
|`ISourceGeneratedDependencyActivator`|[link](./ISourceGeneratedDependencyActivator.md)||
|`ISourceGeneratedLongRunningLoadCache`|[link](./ISourceGeneratedLongRunningLoadCache.md)||



# クラス
|Name|Link|Description|
|:-|:-|:-|
|`BackgroundDependencyLoaderAttribute`|[link](./BackgroundDependencyLoaderAttribute.md)||
|`CachedAttribute`|[link](./CachedAttribute.md)||
|`NullDependencyException`|[link](./CachedAttribute.md#class-nulldependencyexception)||
|`CachedModelDependencyContainer<TModel>`|[link](./CachedModelDependencyContainer.md)||
|`MultipleDependencyLoaderMethodsException`|[link](./DependencyActivator.md#class-multipledependencyloadermethodsexception)||
|`DependencyNotRegisteredException`|[link](./DependencyActivator.md#class-dependencynotregisteredexception)||
|`AccessModifierNotAllowedForMemberException`|[link](./DependencyActivator.md#accessmodifiernotallowedformemberexception)||
|`AccessModifierNotAllowedForCachedValueException`|[link](./DependencyActivator.md#class-accessmodifiernotallowedforcachedvalueexception)||
|`AccessModifierNotAllowedForLoaderMethodException`|[link](./DependencyActivator.md#class-accessmodifiernotallowedforloadermethodexception)||
|`AccessModifierNotAllowedForPropertySetterException`|[link](./DependencyActivator.md#class-accessmodifiernotallowedforpropertysetterexception)||
|`DependencyContainer`|[link](./DependencyContainer.md)||
|`TypeAlreadyCachedException`|[link](./DependencyContainer.md#class-typealreadycachedexception)||
|`ReadOnlyDependencyContainerExtensions`|[link](./IReadOnlyDependencyContainer.md#class-readonlydependencycontainerextensions)||
|`InvokeOnDisposal`|[link](./InvokeOnDisposal.md)||
|`InvokeOnDisposal<T>`|[link](./InvokeOnDisposal.md)||
|`LongRunningLoadAttribute`|[link](./LongRunningLoadAttribute.md)||
|`ObjectUsage<T>`|[link](./ObjectUsage.md)||
|`ResolvedAttribute`|[link](./ResolvedAttribute.md)||
|`PropertyNotWritableException`|[link](./ResolvedAttribute.md#class-propertynotwritableexception)||
|`TimedExpiryCache<TKey, TValue>`|[link](./TimedExpiryCache.md)||
|`TripleBuffer<T>`|[link](./TripleBuffer.md)||



# 構造体
|Name|link|Description|
|:-|:-|:-|
|`CacheInfo`|[link](./CacheInfo.md)||
|`ObjectHandle<T>`|[link](./ObjectHandle.md)||
|`ValueInvokeOnDisposal`|[link](./ValueInvokeOnDisposal.md)||
|`ValueInvokeOnDisposal<T>`|[link](./ValueInvokeOnDisposal.md#struct-valueinvokeondisposalt)||



# 列挙型
|Name|link|Description|
|:-|:-|:-|
|`UsageType`|[link](./ObjectUsage.md#enum-usagetype)||



# デリゲート
|Name|Link|Description|
|:-|:-|:-|
|`InjectDependencyDelegate`|[link](./DependencyActivator.md#delegate-injectdependencydelegate)||
|`CacheDependencyDelegate`|[link](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L223)||