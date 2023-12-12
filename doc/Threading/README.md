# osu.Framework.Threading Doc
- [osu.Framework.Threading Doc](#osuframeworkthreading-doc)
- [クラス](#クラス)
  - [`AudioThread` #](#audiothread-)
  - [`DrawThread` #](#drawthread-)
  - [`GameThread` #](#gamethread-)
  - [`InputThread` #](#inputthread-)
  - [`ScheduledDelegate` #](#scheduleddelegate-)
  - [`Scheduler` #](#scheduler-)
  - [`ThreadedTaskScheduler` #](#threadedtaskscheduler-)
  - [`UpdateThread` #](#updatethread-)
- [列挙型](#列挙型)
  - [`GameThreadState` #](#gamethreadstate-)

# クラス
## `AudioThread` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/AudioThread.cs#L16)
```csharp
public class AudioThread : GameThread
```

## `DrawThread` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/DrawThread.cs#L13)
```csharp
public class DrawThread : GameThread
```

## `GameThread` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/GameThread.cs#L21)
```csharp
public class GameThread
```

## `InputThread` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/InputThread.cs#L10)
```csharp
public class InputThread : GameThread
```

## `ScheduledDelegate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/ScheduledDelegate.cs#L9)
```csharp
public class ScheduledDelegate : IComparable<ScheduledDelegate>
```

## `Scheduler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/Scheduler.cs#L18)
```csharp
public class Scheduler
```

## `ThreadedTaskScheduler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/ThreadedTaskScheduler.cs#L18)
```csharp
public sealed class ThreadedTaskScheduler : TaskScheduler, IDisposable
```

## `UpdateThread` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/UpdateThread.cs#L12)
```csharp
public class UpdateThread : GameThread
```



# 列挙型
## `GameThreadState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Threading/GameThreadState.cs#L8)
```csharp
public enum GameThreadState
```