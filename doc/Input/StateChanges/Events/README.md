# osu.Framework.Input.StateChanges.Events Doc
- [osu.Framework.Input.StateChanges.Events Doc](#osuframeworkinputstatechangesevents-doc)
- [クラス](#クラス)
  - [`ButtonStateChangeEvent<TButton>` #](#buttonstatechangeeventtbutton-)
  - [`InputStateChangeEvent` #](#inputstatechangeevent-)
  - [`JoystickAxisChangeEvent` #](#joystickaxischangeevent-)
  - [`MousePositionChangeEvent` #](#mousepositionchangeevent-)
  - [`MouseScrollChangeEvent` #](#mousescrollchangeevent-)
  - [`TouchStateChangeEvent` #](#touchstatechangeevent-)

# クラス
## `ButtonStateChangeEvent<TButton>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/Events/ButtonStateChangeEvent.cs#L8)
```csharp
public class ButtonStateChangeEvent<TButton> : InputStateChangeEvent
    where TButton : struct
```

## `InputStateChangeEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/Events/InputStateChangeEvent.cs#L13)
```csharp
public abstract class InputStateChangeEvent
```

## `JoystickAxisChangeEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/Events/JoystickAxisChangeEvent.cs#L8)
```csharp
public class JoystickAxisChangeEvent : InputStateChangeEvent
```

## `MousePositionChangeEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/Events/MousePositionChangeEvent.cs#L9)
```csharp
public class MousePositionChangeEvent : InputStateChangeEvent
```

## `MouseScrollChangeEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/Events/MouseScrollChangeEvent.cs#L9)
```csharp
public class MouseScrollChangeEvent : InputStateChangeEvent
```

## `TouchStateChangeEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/Events/TouchStateChangeEvent.cs#L9)
```csharp
public class TouchStateChangeEvent : InputStateChangeEvent
```