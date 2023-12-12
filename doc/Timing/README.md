# osu.Framework.Timing Doc
- [osu.Framework.Timing Doc](#osuframeworktiming-doc)
- [インターフェース](#インターフェース)
  - [`IAdjustableClock` #](#iadjustableclock-)
  - [`IClock` #](#iclock-)
  - [`IFrameBasedClock` #](#iframebasedclock-)
  - [`ISourceChangeableClock` #](#isourcechangeableclock-)
- [クラス](#クラス)
  - [`DecoupleableInterpolatingFramedClock` #](#decoupleableinterpolatingframedclock-)
  - [`DecouplingFramedClock` #](#decouplingframedclock-)
  - [`FramedClock` #](#framedclock-)
  - [`FramedOffsetClock` #](#framedoffsetclock-)
  - [`InterpolatingFramedClock` #](#interpolatingframedclock-)
  - [`ManualClock` #](#manualclock-)
  - [`ManualFramedClock` #](#manualframedclock-)
  - [`OffsetClock` #](#offsetclock-)
  - [`StopwatchClock` #](#stopwatchclock-)
  - [`ThrottledFrameClock` #](#throttledframeclock-)
- [構造体](#構造体)
  - [`FrameTimeInfo` #](#frametimeinfo-)

# インターフェース
## `IAdjustableClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/IAdjustableClock.cs#L9)
```csharp
public interface IAdjustableClock : IClock
```

## `IClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/IClock.cs#L9)
```csharp
public interface IClock
```
## `IFrameBasedClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/IFrameBasedClock.cs#L10)
```csharp
public interface IFrameBasedClock : IClock
```

## `ISourceChangeableClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/ISourceChangeableClock.cs#L9)
```csharp
public interface ISourceChangeableClock : IClock
```

# クラス
## `DecoupleableInterpolatingFramedClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/DecoupleableInterpolatingFramedClock.cs#L20)
```csharp
[Obsolete("This clock implementation is too complex and no longer. Use DecouplingClock instead.")] // can be removed 20240321.
    public class DecoupleableInterpolatingFramedClock : InterpolatingFramedClock, IAdjustableClock
```

## `DecouplingFramedClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/DecouplingFramedClock.cs#L29)
```csharp
public sealed class DecouplingFramedClock : ISourceChangeableClock, IAdjustableClock, IFrameBasedClock
```

## `FramedClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/FramedClock.cs#L15)
```csharp
public class FramedClock : IFrameBasedClock, ISourceChangeableClock
```

## `FramedOffsetClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/FramedOffsetClock.cs#L9)
```csharp
public class FramedOffsetClock : FramedClock
```

## `InterpolatingFramedClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/InterpolatingFramedClock.cs#L12)
```csharp
public class InterpolatingFramedClock : IFrameBasedClock, ISourceChangeableClock // TODO: seal when DecoupleableInterpolatingFramedClock is gone.
```

## `ManualClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/ManualClock.cs#L9)
```csharp
public class ManualClock : IClock
```

## `ManualFramedClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/ManualFramedClock.cs#L9)
```csharp
public class ManualFramedClock : IFrameBasedClock
```

## `OffsetClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/OffsetClock.cs#L6)
```csharp
public class OffsetClock : IClock
```

## `StopwatchClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/StopwatchClock.cs#L10)
```csharp
public class StopwatchClock : Stopwatch, IAdjustableClock
```

## `ThrottledFrameClock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/ThrottledFrameClock.cs#L15)
```csharp
public class ThrottledFrameClock : FramedClock, IDisposable
```



# 構造体
## `FrameTimeInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Timing/FrameTimeInfo.cs#L9)
```csharp
public struct FrameTimeInfo
```