# osu.Framework.Audio Doc
- [osu.Framework.Audio Doc](#osuframeworkaudio-doc)
- [インターフェース](#インターフェース)
  - [`IAdjustableAudioComponent` #](#iadjustableaudiocomponent-)
  - [`IAdjustableResourceStore<T>` #](#iadjustableresourcestoret-)
  - [`IAggregateAudioAdjustment` #](#iaggregateaudioadjustment-)
  - [`IHasAmplitudes` #](#ihasamplitudes-)
- [クラス](#クラス)
  - [`AdjustableAudioComponent` #](#adjustableaudiocomponent-)
  - [`AggregateAdjustmentExtensions` #](#aggregateadjustmentextensions-)
  - [`AudioAdjustments` #](#audioadjustments-)
  - [`AudioCollectionManager<T>` #](#audiocollectionmanagert-)
  - [`AudioComponent` #](#audiocomponent-)
  - [`AudioManager` #](#audiomanager-)
  - [`AdjustableAudioComponentExtensions` #](#adjustableaudiocomponentextensions-)
- [列挙型](#列挙型)
  - [`AdjustableProperty` #](#adjustableproperty-)


# インターフェース
## `IAdjustableAudioComponent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/IAdjustableAudioComponent.cs#L11)
```csharp
public interface IAdjustableAudioComponent : IAggregateAudioAdjustment
```

## `IAdjustableResourceStore<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/IAdjustableResourceStore.cs#L8)
```csharp
public interface IAdjustableResourceStore<T> : IResourceStore<T>, IAdjustableAudioComponent
        where T : AudioComponent
```

## `IAggregateAudioAdjustment` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/IAggregateAudioAdjustment.cs#L11)
```csharp
public interface IAggregateAudioAdjustment
```

## `IHasAmplitudes` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/IHasAmplitudes.cs#L8)
```csharp
public interface IHasAmplitudes
```




# クラス
## `AdjustableAudioComponent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AdjustableAudioComponent.cs#L11)
```csharp
public class AdjustableAudioComponent : AudioComponent, IAdjustableAudioComponent
```

## `AggregateAdjustmentExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AggregateAdjustmentExtensions.cs#L9)
```csharp
public static class AggregateAdjustmentExtensions
```

## `AudioAdjustments` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AudioAdjustments.cs#L15)
```csharp
public class AudioAdjustments : IAdjustableAudioComponent
```

## `AudioCollectionManager<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AudioCollectionManager.cs#L12)
```csharp
public class AudioCollectionManager<T> : AdjustableAudioComponent, IBassAudio
        where T : AudioComponent
```

## `AudioComponent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AudioComponent.cs#L19)
```csharp
public abstract class AudioComponent : IDisposable, IUpdateable
```

## `AudioManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AudioManager.cs#L28)
```csharp
public class AudioManager : AudioCollectionManager<AudioComponent>
```

## `AdjustableAudioComponentExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/IAdjustableAudioComponent.cs#L66)
```csharp
public static class AdjustableAudioComponentExtensions
```






# 列挙型
## `AdjustableProperty` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/AdjustableAudioComponent.cs#L122)
```csharp
public enum AdjustableProperty
```


