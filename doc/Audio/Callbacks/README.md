# osu.Framework.Audio.Callbacks Doc
- [osu.Framework.Audio.Callbacks Doc](#osuframeworkaudiocallbacks-doc)
- [インターフェース](#インターフェース)
  - [`IFileProcedures` #](#ifileprocedures-)
- [クラス](#クラス)
  - [`BassCallback` #](#basscallback-)
  - [`DataStreamFileProcedures` #](#datastreamfileprocedures-)
  - [`FileCallbacks` #](#filecallbacks-)
  - [`SyncCallback ` #](#synccallback--)


# インターフェース
## `IFileProcedures` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/IFileProcedures.cs#L12)
```csharp
public interface IFileProcedures
```




# クラス
## `BassCallback` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/BassCallback.cs#L15)
```csharp
public abstract class BassCallback : IDisposable
```

## `DataStreamFileProcedures` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/DataStreamFileProcedures.cs#L12)
```csharp
public class DataStreamFileProcedures : IFileProcedures
```

## `FileCallbacks` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/FileCallbacks.cs#L18)
```csharp
public class FileCallbacks : BassCallback
```

## `SyncCallback ` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/SyncCallback.cs#L15)
```csharp
public class SyncCallback : BassCallback
```

