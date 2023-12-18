- [Class DependencyActivator #](#class-dependencyactivator-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
- [Class MultipleDependencyLoaderMethodsException #](#class-multipledependencyloadermethodsexception-)
  - [Namespace](#namespace-1)
  - [Implements](#implements)
  - [Syntax](#syntax-1)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
- [Class DependencyNotRegisteredException #](#class-dependencynotregisteredexception-)
  - [Namespace](#namespace-2)
  - [Implements](#implements-1)
  - [Syntax](#syntax-2)
  - [Constructor](#constructor-1)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
- [Class AccessModifierNotAllowedForMemberException #](#class-accessmodifiernotallowedformemberexception-)
  - [Namespace](#namespace-3)
  - [Implements](#implements-2)
  - [Syntax](#syntax-3)
  - [Constructor](#constructor-2)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-2)
- [Class AccessModifierNotAllowedForCachedValueException #](#class-accessmodifiernotallowedforcachedvalueexception-)
  - [Namespace](#namespace-4)
  - [Implements](#implements-3)
  - [Syntax](#syntax-4)
  - [Constructor](#constructor-3)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-3)
- [Class AccessModifierNotAllowedForLoaderMethodException #](#class-accessmodifiernotallowedforloadermethodexception-)
  - [Namespace](#namespace-5)
  - [Implements](#implements-4)
  - [Syntax](#syntax-5)
  - [Constructor](#constructor-4)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-4)
- [Class AccessModifierNotAllowedForPropertySetterException #](#class-accessmodifiernotallowedforpropertysetterexception-)
  - [Namespace](#namespace-6)
  - [Implements](#implements-5)
  - [Syntax](#syntax-6)
  - [Constructor](#constructor-5)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-5)
- [Delegate InjectDependencyDelegate #](#delegate-injectdependencydelegate-)
  - [Namespace](#namespace-7)
  - [Syntax](#syntax-7)
      - [Arguments](#arguments-6)
- [Delegate CacheDependencyDelegate #](#delegate-cachedependencydelegate-)
  - [Namespace](#namespace-8)
  - [Syntax](#syntax-8)
      - [Arguments](#arguments-7)



# Class DependencyActivator [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L26)
オブジェクトの依存関係をマージし、依存関係をオブジェクトに注入するメソッドを提供するヘルパー クラス。<br>
依存関係をオブジェクトにマージ/注入するプロセスは、最も派生したものから最も派生したものへと「ボトムアップ」方式で行われる。<br>
例えば。 `Drawable -> CompositeDrawable -> Toolbar` など...<br>
依存関係の注入は、次の 2 つのプロセスに順序付けされる：<br>
1. [ResolvedAttribute]()でマークされたプロパティに挿入する。
2. [BackgroundDependencyLoaderAttribute]()でマークされたメソッドを呼び出す。


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
internal class DependencyActivator
```



---
# Class MultipleDependencyLoaderMethodsException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L154)
1 つのオブジェクトに複数の[BackgroundDependencyLoaderAttribute]()が存在する場合に発生する。


## Namespace
osu.Framework.Allocation


## Implements
[Exception]()


## Syntax
```csharp
public class MultipleDependencyLoaderMethodsException : Exception
```


## Constructor
#### Declaration
```csharp
public MultipleDependencyLoaderMethodsException(Type type)
    : base($"The type {type.ReadableName()} has more than one method marked with a {nameof(BackgroundDependencyLoaderAttribute)}."
        + "Any given type may only have one such method.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()||



---
# Class DependencyNotRegisteredException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L168)
オブジェクトが依存関係の解決を要求したが、依存関係が存在しない場合に発生する。<br>
これは、親[CompositeDrawable]()から[CompositeDrawable.CreateChildDependency]()または[CachedAttribute]()によって依存関係が登録されていないことが原因で発生する。


## Namespace
osu.Framework.Allocation


## Implements
[Exception]()


## Syntax
```csharp
public class DependencyNotRegisteredException : Exception
```


## Constructor
#### Declaration
```csharp
public DependencyNotRegisteredException(Type type, Type requestedType)
    : base($"The type {type.ReadableName()} has a dependency on {requestedType.ReadableName()}, but the dependency is not registered.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()||
|`requestedType`|[Type]()||



---
# Class AccessModifierNotAllowedForMemberException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L179)
許容できないアクセス修飾子を持つメンバーに対して依存関係に関連した操作が発生したときに発生する。


## Namespace
osu.Framework.Allocation


## Implements
[InvalidOperationException]()


## Syntax
```csharp
public abstract class AccessModifierNotAllowedForMemberException : InvalidOperationException
```


## Constructor
#### Declaration
```csharp
protected AccessModifierNotAllowedForMemberException(AccessModifier modifier, MemberInfo member, string description)
    : base($"The access modifier(s) [ {modifier.ToString()} ] are not allowed on \"{member.DeclaringType.ReadableName()}.{member.Name}\". {description}")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`modifier`|[AccessModifier]()||
|`member`|[MemberInfo]()||
|`description`|string||



---
# Class AccessModifierNotAllowedForCachedValueException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L190)
[CachedAttribute]()が添付された非プライベートおよび非読み取り専用フィールドをキャッシュしようとしたときに発生する。


## Namespace
osu.Framework.Allocation


## Implements
[AccessModifierNotAllowedForMemberException]()


## Syntax
```csharp
public class AccessModifierNotAllowedForCachedValueException : AccessModifierNotAllowedForMemberException
```


## Constructor
#### Declaration
```csharp
public AccessModifierNotAllowedForCachedValueException(AccessModifier modifier, MemberInfo member)
    : base(modifier, member, $"A field with an attached {nameof(CachedAttribute)} must be private, readonly,"
        + " or be an auto-property with a getter and private (or non-existing) setter.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`modifier`|[AccessModifier]()||
|`member`|[MemberInfo]()||



---
# Class AccessModifierNotAllowedForLoaderMethodException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L202)
[BackgroundDependencyLoaderAttribute]()が添付されたメソッドがプライベートではない場合に発生する。


## Namespace
osu.Framework.Allocation


## Implements
[AccessModifierNotAllowedForMemberException]()


## Syntax
```csharp
public class AccessModifierNotAllowedForLoaderMethodException : AccessModifierNotAllowedForMemberException
```


## Constructor
#### Declaration
```csharp
public AccessModifierNotAllowedForLoaderMethodException(AccessModifier modifier, MemberInfo member)
    : base(modifier, member, $"A method with an attached {nameof(BackgroundDependencyLoaderAttribute)} must be private.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`modifier`|[AccessModifier]()||
|`member`|[MemberInfo]()||



---
# Class AccessModifierNotAllowedForPropertySetterException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L213)
[ResolvedAttribute]()が添付されたプロパティのセッターがプライベートではない場合に発生する。


## Namespace
osu.Framework.Allocation


## Implements
[AccessModifierNotAllowedForMemberException]()


## Syntax
```csharp
public class AccessModifierNotAllowedForPropertySetterException : AccessModifierNotAllowedForMemberException
```


## Constructor
#### Declaration
```csharp
public AccessModifierNotAllowedForPropertySetterException(AccessModifier modifier, MemberInfo member)
    : base(modifier, member, $"A property with an attached {nameof(ResolvedAttribute)} must have a private setter.")
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`modifier`|[AccessModifier]()||
|`member`|[MemberInfo]()||



---
# Delegate InjectDependencyDelegate [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L221)


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public delegate void InjectDependencyDelegate(object target, IReadOnlyDependencyContainer dependencies);
```

#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`target`|object||
|`dependencies`|[IReadOnlyDependencyContainer]()||



---
# Delegate CacheDependencyDelegate [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyActivator.cs#L223)


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public delegate IReadOnlyDependencyContainer CacheDependencyDelegate(object target, IReadOnlyDependencyContainer existingDependencies, CacheInfo info);
```


#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`target`|object||
|`existingDependencies`|[IReadOnlyDependencyContainer]()||
|`info`|[CacheInfo]()||