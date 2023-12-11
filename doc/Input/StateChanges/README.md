# osu.Framework.Input.StateChanges Doc
- [osu.Framework.Input.StateChanges Doc](#osuframeworkinputstatechanges-doc)
- [インターフェース](#インターフェース)
  - [`IInput` #](#iinput-)
  - [`IInputStateChangeHandler` #](#iinputstatechangehandler-)
  - [`ISourcedFromTouch` #](#isourcedfromtouch-)
- [クラス](#クラス)
  - [`ButtonInput` #](#buttoninput-)
  - [`ButtonInputEntry<TButton>` #](#buttoninputentrytbutton-)
  - [`JoystickAxisInput` #](#joystickaxisinput-)
  - [`JoystickButtonInput` #](#joystickbuttoninput-)
  - [`KeyboardKeyInput` #](#keyboardkeyinput-)
  - [`MidiKeyInput` #](#midikeyinput-)
  - [`MouseButtonInput` #](#mousebuttoninput-)
  - [`MouseButtonInputFromTouch` #](#mousebuttoninputfromtouch-)
  - [`MousePositionAbsoluteInput` #](#mousepositionabsoluteinput-)
  - [`MousePositionAbsoluteInputFromTouch` #](#mousepositionabsoluteinputfromtouch-)
  - [`MousePositionRelativeInput` #](#mousepositionrelativeinput-)
  - [`MouseScrollRelativeInput` #](#mousescrollrelativeinput-)
  - [`TabletAuxiliaryButtonInput` #](#tabletauxiliarybuttoninput-)
  - [`TabletPenButtonInput` #](#tabletpenbuttoninput-)
  - [`TouchInput` #](#touchinput-)
- [列挙型](#列挙型)
  - [`ButtonStateChangeKind` #](#buttonstatechangekind-)

# インターフェース
## `IInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/IInput.cs#L11)
```csharp
public interface IInput
```

## `IInputStateChangeHandler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/IInputStateChangeHandler.cs#L12)
```csharp
public interface IInputStateChangeHandler
```

## `ISourcedFromTouch` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/ISourcedFromTouch.cs#L12)
```csharp
public interface ISourcedFromTouch : IInput
```



# クラス
## `ButtonInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/ButtonInput.cs#L15)
```csharp
public abstract class ButtonInput<TButton> : IInput
    where TButton : struct
```

## `ButtonInputEntry<TButton>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/ButtonInputEntry.cs#L10)
```csharp
public struct ButtonInputEntry<TButton>
    where TButton : struct
```

## `JoystickAxisInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/JoystickAxisInput.cs#L14)
```csharp
public class JoystickAxisInput : IInput
```

## `JoystickButtonInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/JoystickButtonInput.cs#L9)
```csharp
public class JoystickButtonInput : ButtonInput<JoystickButton>
```

## `KeyboardKeyInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/KeyboardKeyInput.cs#L10)
```csharp
public class KeyboardKeyInput : ButtonInput<Key>
```

## `MidiKeyInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MidiKeyInput.cs#L13)
```csharp
public class MidiKeyInput : ButtonInput<MidiKey>
```

## `MouseButtonInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MouseButtonInput.cs#L10)
```csharp
public class MouseButtonInput : ButtonInput<MouseButton>
```

## `MouseButtonInputFromTouch` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MouseButtonInputFromTouch.cs#L9)
```csharp
public class MouseButtonInputFromTouch : MouseButtonInput, ISourcedFromTouch
```

## `MousePositionAbsoluteInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MousePositionAbsoluteInput.cs#L17)
```csharp
public class MousePositionAbsoluteInput : IInput
```

## `MousePositionAbsoluteInputFromTouch` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MousePositionAbsoluteInputFromTouch.cs#L8)
```csharp
public class MousePositionAbsoluteInputFromTouch : MousePositionAbsoluteInput, ISourcedFromTouch
```

## `MousePositionRelativeInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MousePositionRelativeInput.cs#L14)
```csharp
public class MousePositionRelativeInput : IInput
```

## `MouseScrollRelativeInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/MouseScrollRelativeInput.cs#L14)
```csharp
public class MouseScrollRelativeInput : IInput
```

## `TabletAuxiliaryButtonInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/TabletAuxiliaryButtonInput.cs#L9)
```csharp
public class TabletAuxiliaryButtonInput : ButtonInput<TabletAuxiliaryButton>
```

## `TabletPenButtonInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/TabletPenButtonInput.cs#L9)
```csharp
public class TabletPenButtonInput : ButtonInput<TabletPenButton>
```

## `TouchInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/TouchInput.cs#L14)
```csharp
public class TouchInput : IInput
```



# 列挙型
## `ButtonStateChangeKind` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/StateChanges/ButtonStateChangeKind.cs#L9)
```csharp
public enum ButtonStateChangeKind
```