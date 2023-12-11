# osu.Framework.Input.Events Doc
- [osu.Framework.Input.Events Doc](#osuframeworkinputevents-doc)
- [クラス](#クラス)
  - [`ClickEvent` #](#clickevent-)
  - [`DoubleClickEvent` #](#doubleclickevent-)
  - [`DragEndEvent` #](#dragendevent-)
  - [`DragEvent` #](#dragevent-)
  - [`DragStartEvent` #](#dragstartevent-)
  - [`FocusEvent` #](#focusevent-)
  - [`FocusLostEvent` #](#focuslostevent-)
  - [`HoverEvent` #](#hoverevent-)
  - [`HoverLostEvent` #](#hoverlostevent-)
  - [`JoystickAxisMoveEvent` #](#joystickaxismoveevent-)
  - [`JoystickButtonEvent` #](#joystickbuttonevent-)
  - [`JoystickEvent` #](#joystickevent-)
  - [`JoystickPressEvent` #](#joystickpressevent-)
  - [`JoystickReleaseEvent` #](#joystickreleaseevent-)
  - [`KeyBindingEvent<T>` #](#keybindingeventt-)
  - [`KeyBindingPressEvent<T>` #](#keybindingpresseventt-)
  - [`KeyBindingReleaseEvent<T>` #](#keybindingreleaseeventt-)
  - [`KeyBindingScrollEvent<T>` #](#keybindingscrolleventt-)
  - [`KeyDownEvent` #](#keydownevent-)
  - [`KeyUpEvent` #](#keyupevent-)
  - [`KeyboardEvent` #](#keyboardevent-)
  - [`MidiDownEvent` #](#mididownevent-)
  - [`MidiEvent` #](#midievent-)
  - [`MidiUpEvent` #](#midiupevent-)
  - [`MouseButtonEvent` #](#mousebuttonevent-)
  - [`MouseDownEvent` #](#mousedownevent-)
  - [`MouseEvent` #](#mouseevent-)
  - [`MouseMoveEvent` #](#mousemoveevent-)
  - [`MouseUpEvent` #](#mouseupevent-)
  - [`ScrollEvent` #](#scrollevent-)
  - [`TabletAuxiliaryButtonEvent` #](#tabletauxiliarybuttonevent-)
  - [`TabletAuxiliaryPressEvent` #](#tabletauxiliarypressevent-)
  - [`TabletAuxiliaryReleaseEvent` #](#tabletauxiliaryreleaseevent-)
  - [`TabletEvent` #](#tabletevent-)
  - [`TabletPenButtonEvent` #](#tabletpenbuttonevent-)
  - [`TabletPenButtonPressEvent` #](#tabletpenbuttonpressevent-)
  - [`TabletPenButtonReleaseEvent` #](#tabletpenbuttonreleaseevent-)
  - [`TouchDownEvent` #](#touchdownevent-)
  - [`TouchEvent` #](#touchevent-)
  - [`TouchMoveEvent` #](#touchmoveevent-)
  - [`TouchUpEvent` #](#touchupevent-)
  - [`UIEvent` #](#uievent-)

# クラス
## `ClickEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/ClickEvent.cs#L13)
```csharp
public class ClickEvent : MouseButtonEvent
```

## `DoubleClickEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/DoubleClickEvent.cs#L13)
```csharp
public class DoubleClickEvent : MouseButtonEvent
```

## `DragEndEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/DragEndEvent.cs#L14)
```csharp
public class DragEndEvent : MouseButtonEvent
```

## `DragEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/DragEvent.cs#L14)
```csharp
public class DragEvent : MouseButtonEvent
```

## `DragStartEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/DragStartEvent.cs#L13)
```csharp
public class DragStartEvent : MouseButtonEvent
```

## `FocusEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/FocusEvent.cs#L12)
```csharp
public class FocusEvent : UIEvent
```

## `FocusLostEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/FocusLostEvent.cs#L12)
```csharp
public class FocusLostEvent : UIEvent
```

## `HoverEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/HoverEvent.cs#L12)
```csharp
public class HoverEvent : MouseEvent
```

## `HoverLostEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/HoverLostEvent.cs#L12)
```csharp
public class HoverLostEvent : MouseEvent
```

## `JoystickAxisMoveEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/JoystickAxisMoveEvent.cs#L12)
```csharp
public class JoystickAxisMoveEvent : JoystickEvent
```

## `JoystickButtonEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/JoystickButtonEvent.cs#L12)
```csharp
public abstract class JoystickButtonEvent : JoystickEvent
```

## `JoystickEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/JoystickEvent.cs#L10)
```csharp
public abstract class JoystickEvent : UIEvent
```

## `JoystickPressEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/JoystickPressEvent.cs#L11)
```csharp
public class JoystickPressEvent : JoystickButtonEvent
```

## `JoystickReleaseEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/JoystickReleaseEvent.cs#L11)
```csharp
public class JoystickReleaseEvent : JoystickButtonEvent
```

## `KeyBindingEvent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyBindingEvent.cs#L12)
```csharp
public abstract class KeyBindingEvent<T> : UIEvent where T : struct
```

## `KeyBindingPressEvent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyBindingPressEvent.cs#L12)
```csharp
public class KeyBindingPressEvent<T> : KeyBindingEvent<T> where T : struct
```

## `KeyBindingReleaseEvent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyBindingReleaseEvent.cs#L12)
```csharp
public class KeyBindingReleaseEvent<T> : KeyBindingEvent<T> where T : struct
```

## `KeyBindingScrollEvent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyBindingScrollEvent.cs#L12)
```csharp
public class KeyBindingScrollEvent<T> : KeyBindingEvent<T> where T : struct
```

## `KeyDownEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyDownEvent.cs#L13)
```csharp
public class KeyDownEvent : KeyboardEvent
```

## `KeyUpEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyUpEvent.cs#L12)
```csharp
public class KeyUpEvent : KeyboardEvent
```

## `KeyboardEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/KeyboardEvent.cs#L14)
```csharp
public abstract class KeyboardEvent : UIEvent
```

## `MidiDownEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MidiDownEvent.cs#L8)
```csharp
public class MidiDownEvent : MidiEvent
```

## `MidiEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MidiEvent.cs#L10)
```csharp
public abstract class MidiEvent : UIEvent
```

## `MidiUpEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MidiUpEvent.cs#L8)
```csharp
public class MidiUpEvent : MidiEvent
```

## `MouseButtonEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MouseButtonEvent.cs#L14)
```csharp
public abstract class MouseButtonEvent : MouseEvent
```

## `MouseDownEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MouseDownEvent.cs#L13)
```csharp
public class MouseDownEvent : MouseButtonEvent
```

## `MouseEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MouseEvent.cs#L13)
```csharp
public abstract class MouseEvent : UIEvent
```

## `MouseMoveEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MouseMoveEvent.cs#L12)
```csharp
public class MouseMoveEvent : MouseEvent
```

## `MouseUpEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/MouseUpEvent.cs#L13)
```csharp
public class MouseUpEvent : MouseButtonEvent
```

## `ScrollEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/ScrollEvent.cs#L13)
```csharp
public class ScrollEvent : MouseEvent
```

## `TabletAuxiliaryButtonEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletAuxiliaryButtonEvent.cs#L12)
```csharp
public abstract class TabletAuxiliaryButtonEvent : TabletEvent
```

## `TabletAuxiliaryPressEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletAuxiliaryButtonPressEvent.cs#L11)
```csharp
public class TabletAuxiliaryButtonPressEvent : TabletAuxiliaryButtonEvent
```

## `TabletAuxiliaryReleaseEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletAuxiliaryButtonReleaseEvent.cs#L11)
```csharp
public class TabletAuxiliaryButtonReleaseEvent : TabletAuxiliaryButtonEvent
```

## `TabletEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletEvent.cs#L9)
```csharp
public abstract class TabletEvent : UIEvent
```

## `TabletPenButtonEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletPenButtonEvent.cs#L12)
```csharp
public abstract class TabletPenButtonEvent : TabletEvent
```

## `TabletPenButtonPressEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletPenButtonPressEvent.cs#L11)
```csharp
public class TabletPenButtonPressEvent : TabletPenButtonEvent
```

## `TabletPenButtonReleaseEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TabletPenButtonReleaseEvent.cs#L11)
```csharp
public class TabletPenButtonReleaseEvent : TabletPenButtonEvent
```

## `TouchDownEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TouchDownEvent.cs#L8)
```csharp
public class TouchDownEvent : TouchEvent
```

## `TouchEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TouchEvent.cs#L13)
```csharp
public class TouchEvent : UIEvent
```

## `TouchMoveEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TouchMoveEvent.cs#L12)
```csharp
public class TouchMoveEvent : TouchEvent
```

## `TouchUpEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/TouchUpEvent.cs#L9)
```csharp
public class TouchUpEvent : TouchEvent
```

## `UIEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Events/UIEvent.cs#L20)
```csharp
public abstract class UIEvent
```