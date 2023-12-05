# osu.Framework.Configuration Doc
- [osu.Framework.Configuration Doc](#osuframeworkconfiguration-doc)
- [インターフェース](#インターフェース)
  - [`IConfigManager` #](#iconfigmanager-)
- [クラス](#クラス)
  - [`ConfigManager<TLookup>` #](#configmanagertlookup-)
  - [`ConfigManager` #](#configmanager-)
  - [`FrameworkConfigManager` #](#frameworkconfigmanager-)
  - [`FrameworkDebugConfigManager` #](#frameworkdebugconfigmanager-)
  - [`IniConfigManager<TLookup>` #](#iniconfigmanagertlookup-)
- [列挙型](#列挙型)
  - [`FrameSync` #](#framesync-)
  - [`FrameworkSetting` #](#frameworksetting-)
  - [`DebugSetting` #](#debugsetting-)
  - [`RendererType` #](#renderertype-)
  - [`WindowMode` #](#windowmode-)


# インターフェース
## `IConfigManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/IConfigManager.cs#L6)
```csharp
public interface IConfigManager
```



# クラス
## `ConfigManager<TLookup>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/ConfigManager.cs#L18)
```csharp
public abstract class ConfigManager<TLookup> : ConfigManager, ITrackableConfigManager
        where TLookup : struct, Enum
```

## `ConfigManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/ConfigManager.cs#L339)
```csharp
public abstract class ConfigManager : IDisposable
```

## `FrameworkConfigManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameworkConfigManager.cs#L18)
```csharp
public class FrameworkConfigManager : IniConfigManager<FrameworkSetting>
```

## `FrameworkDebugConfigManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameworkDebugConfig.cs#L6)
```csharp
public class FrameworkDebugConfigManager : IniConfigManager<DebugSetting>
```

## `IniConfigManager<TLookup>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/IniConfigManager.cs#L19)
```csharp
public class IniConfigManager<TLookup> : ConfigManager<TLookup>
```





# 列挙型
## `FrameSync` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameSync.cs#L8)
```csharp
public enum FrameSync
```

## `FrameworkSetting` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameworkConfigManager.cs#L76)
```csharp
public enum FrameworkSetting
```

## `DebugSetting` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameworkDebugConfig.cs#L23)
```csharp
public enum DebugSetting
```

## `RendererType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/RendererType.cs#L8)
```csharp
public enum RendererType
```

## `WindowMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/WindowMode.cs#L6)
```csharp
public enum WindowMode
```


