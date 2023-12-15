# osu.Framework Doc
- [osu.Framework Doc](#osuframework-doc)
- [Interface](#interface)
  - [`IStateful<T>` #](#istatefult-)
  - [`IUpdateable` #](#iupdateable-)
- [Class](#class)
  - [`FrameworkEnvironment` #](#frameworkenvironment-)
  - [`Game` #](#game-)
  - [`Host` #](#host-)
  - [`HostOptions` #](#hostoptions-)
  - [`RuntimeInfo` #](#runtimeinfo-)

# Interface
## `IStateful<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IStateful.cs#L12)
状態を持ち、外部コンシューマが現在の状態を変更できるようにするオブジェクト。
```csharp
public interface IStateful<T>
    where T : struct
```

## `IUpdateable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IUpdateable.cs#L6)
```csharp
public interface IUpdateable
```


# Class
## `FrameworkEnvironment` [#]()
```csharp
public static class FrameworkEnvironment
```

## `Game` [#]()
```csharp
public abstract partial class Game : Container, IKeyBindingHandler<FrameworkAction>, IKeyBindingHandler<PlatformAction>, IHandleGlobalKeyboardInput
```

## `Host` [#]()
```csharp
public static class Host
```

## `HostOptions` [#]()
[Host]()のさまざまな構成プロパティ。
```csharp
public class HostOptions
```

## `RuntimeInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/RuntimeInfo.cs#L10)
```csharp
public static class RuntimeInfo
```