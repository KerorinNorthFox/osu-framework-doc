# osu.Framework Doc
- [osu.Framework Doc](#osuframework-doc)
- [インターフェース](#インターフェース)
  - [`IStateful<T>` #](#istatefult-)
  - [`IUpdateable` #](#iupdateable-)
- [クラス](#クラス)
  - [`FrameworkEnvironment` #](#frameworkenvironment-)
  - [`Game` #](#game-)
  - [`Host` #](#host-)
  - [`HostOptions` #](#hostoptions-)
  - [`RuntimeInfo` #](#runtimeinfo-)

# インターフェース
## `IStateful<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IStateful.cs#L12)
```csharp
public interface IStateful<T>
    where T : struct
```

## `IUpdateable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IUpdateable.cs#L6)
```csharp
public interface IUpdateable
```

# クラス
## `FrameworkEnvironment` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L9)
```csharp
public static class FrameworkEnvironment
```

## `Game` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L31)
```csharp
public abstract partial class Game : Container, IKeyBindingHandler<FrameworkAction>, IKeyBindingHandler<PlatformAction>, IHandleGlobalKeyboardInput
```

## `Host` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Host.cs#L15)
```csharp
public static class Host
```

## `HostOptions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/HostOptions.cs#L11)
```csharp
public class HostOptions
```

## `RuntimeInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/RuntimeInfo.cs#L10)
```csharp
public static class RuntimeInfo
```