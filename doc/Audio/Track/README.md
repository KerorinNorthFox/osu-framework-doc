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






<!-- 
# osu.Framework.Audio.Track
## public readonly struct `ChannelAmplitudes`
オーディオチャネルのチャネルごとおよび周波数ごとの振幅を提供する情報の集合。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ChannelAmplitudes.cs)
### Property
|name|type|access|usage|
|:-|:-|:-|:-|
|const `AMPLITUDES_SIZE`=256|int||[FrequencyAmplitudes]()データの長さ。|
|`LeftChannel`|float|readonly|左チャンネルの振幅 (0..1)。|
|`RightChannel`|float|readonly|右チャンネルの振幅 (0..1)。|
|`Maximum`|float||左右のチャンネルの最大振幅 (0..1)。|
|`Average`|float||左右のチャンネルの平均振幅 (0..1)。|
|`FrequencyAmplitudes`|ReadOnlyMemory\<float\>|readonly|可聴スペクトル (0Hz ～ 20,000Hz) の ~78Hz ステップごとの両方のチャネルの平均周波数を含む 256 個の長さのビンの配列。|
|static `Empty`|ChannelAmplitudes|g||
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`ChannelAmplitudes`|float leftChannel=0, float rightChannel=0, float[] amplitudes=null|void||


## public abstract class `Track` : AdjustableAudioComponent, ITrack, IAudioChannel
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/Track.cs)
### Property
|name|type|access|usage|
|:-|:-|:-|:-|
|event `Completed`|Action?|||
|event `Failed`|Action?|||
|virtual `IsDummyDevice`|bool|||
|`RestartPoint`|double|||
|virtual `Looping`|bool|||
|`Name`|string|g||
|abstract `CurrentTime`|double|g||
|`Length`|double|||
|virtual `Bitrate`|int?|||
|abstract `IsRunning`|bool|g||
|virtual `Rate`|double|||
|`IsReversed`|bool|||
|||||
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|virtual `Reset`||void|このトラックを論理的なデフォルト状態にリセットする。|
|`Restart`||void|調整を保持したまま、このトラックを`RestartPoint`から再開する。|
|`RestartAsync`||Task||
|virtual `ResetSpeedAdjustments`||void||
|abstract `Seek`|double seek|bool|新しいポジションを目指す。|
|abstract `SeekAsync`|double seek|Task\<bool\>||
|abstract `StartAsync`||Task||
|abstract `Start`||void||
|abstract `StopAsync`||Task||
|abstract `Stop`||void||

 -->
