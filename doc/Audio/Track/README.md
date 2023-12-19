# osu.Framework.Audio.Track Doc

# インターフェース
## `ITrack` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ITrack.cs#L12)
```csharp
public interface ITrack : IAdjustableClock, IHasAmplitudes, IAdjustableAudioComponent
```

## `ITrackStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ITrackStore.cs#L6)
```csharp
public interface ITrackStore : IAdjustableResourceStore<Track>
```


# クラス
## `Track` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/Track.cs#L12)
```csharp
public abstract class Track : AdjustableAudioComponent, ITrack, IAudioChannel
```

## `TrackBass` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/TrackBass.cs#L21)
```csharp
public sealed class TrackBass : Track, IBassAudio, IBassAudioChannel
```

## `TrackVirtual` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/TrackVirtual.cs#L10)
```csharp
public sealed class TrackVirtual : Track
```

## `Waveform` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/Waveform.cs#L21)
```csharp
public class Waveform : IDisposable
```




# 構造体
## `ChannelAmplitudes` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ChannelAmplitudes.cs#L13)
```csharp
public readonly struct ChannelAmplitudes
```