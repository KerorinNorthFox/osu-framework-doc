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
## `IStateful<T>` [#](./IStateful.md)
状態を持ち、外部コンシューマが現在の状態を変更できるようにするオブジェクト。
```csharp
public interface IStateful<T>
    where T : struct
```

## `IUpdateable` [#](./IUpdateable.md)
```csharp
public interface IUpdateable
```


# Class
## `FrameworkEnvironment` [#](./FrameworkEnvironment.md)
```csharp
public static class FrameworkEnvironment
```

## `Game` [#](./Game.md)
```csharp
public abstract partial class Game : Container, IKeyBindingHandler<FrameworkAction>, IKeyBindingHandler<PlatformAction>, IHandleGlobalKeyboardInput
```

## `Host` [#](./Host.md)
```csharp
public static class Host
```

## `HostOptions` [#](./HostOptions.md)
[Host]()のさまざまな構成プロパティ。
```csharp
public class HostOptions
```

## `RuntimeInfo` [#](./RuntimeInfo.md)
```csharp
public static class RuntimeInfo
```