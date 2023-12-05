# osu.Framework.Configuration.Tracking Doc
- [osu.Framework.Configuration.Tracking Doc](#osuframeworkconfigurationtracking-doc)
- [インターフェース](#インターフェース)
  - [`ITrackableConfigManager` #](#itrackableconfigmanager-)
  - [`ITrackedSetting` #](#itrackedsetting-)
- [クラス](#クラス)
  - [`SettingDescription` #](#settingdescription-)
  - [`TrackedSetting<TValue>` #](#trackedsettingtvalue-)
  - [`TrackedSettings` #](#trackedsettings-)


# インターフェース
## `ITrackableConfigManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/Tracking/ITrackableConfigManager.cs#L11)
```csharp
public interface ITrackableConfigManager : IConfigManager
```

## `ITrackedSetting` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/Tracking/ITrackedSetting.cs#L12)
```csharp
public interface ITrackedSetting
```




# クラス
## `SettingDescription` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/Tracking/SettingDescription.cs#L11)
```csharp
public class SettingDescription
```

## `TrackedSetting<TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/Tracking/TrackedSetting.cs#L15)
```csharp
public abstract class TrackedSetting<TValue> : ITrackedSetting
```

## `TrackedSettings` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/Tracking/TrackedSettings.cs#L11)
```csharp
public class TrackedSettings : List<ITrackedSetting>
```

