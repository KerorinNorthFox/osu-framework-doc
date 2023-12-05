# osu.Framework.Graphics.Audio Doc
- [osu.Framework.Graphics.Audio Doc](#osuframeworkgraphicsaudio-doc)
- [クラス](#クラス)
  - [`DrawableAudioMixer` #](#drawableaudiomixer-)
  - [`DrawableAudioWrapper` #](#drawableaudiowrapper-)
  - [`DrawableSample` #](#drawablesample-)
  - [`DrawableTrack` #](#drawabletrack-)
  - [`WaveformGraph` #](#waveformgraph-)

# クラス
## `DrawableAudioMixer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Audio/DrawableAudioMixer.cs#L16)
```csharp
public partial class DrawableAudioMixer : AudioContainer, IAudioMixer
```

## `DrawableAudioWrapper` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Audio/DrawableAudioWrapper.cs#L21)
```csharp
[Cached(typeof(IAggregateAudioAdjustment))]
public abstract partial class DrawableAudioWrapper : CompositeDrawable, IAdjustableAudioC
```

## `DrawableSample` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Audio/DrawableSample.cs#L14)
```csharp
public partial class DrawableSample : DrawableAudioWrapper, ISample
```

## `DrawableTrack` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Audio/DrawableTrack.cs#L16)
```csharp
public partial class DrawableTrack : DrawableAudioWrapper, ITrack
```

## `WaveformGraph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Audio/WaveformGraph.cs#L27)
```csharp
public partial class WaveformGraph : Drawable
```



