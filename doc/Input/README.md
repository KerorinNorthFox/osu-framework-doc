# osu.Framework.Input Doc
- [osu.Framework.Input Doc](#osuframeworkinput-doc)
- [インターフェース](#インターフェース)
  - [`IHandleGlobalKeyboardInput` #](#ihandleglobalkeyboardinput-)
  - [`IRequireHighFrequencyMousePosition` #](#irequirehighfrequencymouseposition-)
  - [`ISourceGeneratedHandleInputCache` #](#isourcegeneratedhandleinputcache-)
  - [`ISuppressKeyEventLogging` #](#isuppresskeyeventlogging-)
- [クラス](#クラス)
  - [`ButtonEventManager<TButton>` #](#buttoneventmanagertbutton-)
  - [`CustomInputManager` #](#custominputmanager-)
  - [`InputManager` #](#inputmanager-)
  - [`InputResampler` #](#inputresampler-)
  - [`JoystickAxisEventManager` #](#joystickaxiseventmanager-)
  - [`JoystickButtonEventManager` #](#joystickbuttoneventmanager-)
  - [`KeyEventManager` #](#keyeventmanager-)
  - [`MidiKeyEventManager` #](#midikeyeventmanager-)
  - [`MouseButtonEventManager` #](#mousebuttoneventmanager-)
  - [`PassThroughInputManager` #](#passthroughinputmanager-)
  - [`PlatformActionContainer` #](#platformactioncontainer-)
  - [`ReadableKeyCombinationProvider` #](#readablekeycombinationprovider-)
  - [`TabletAuxiliaryButtonEventManager` #](#tabletauxiliarybuttoneventmanager-)
  - [`TabletPenButtonEventManager` #](#tabletpenbuttoneventmanager-)
  - [`TextInputSource` #](#textinputsource-)
  - [`TouchEventManager` #](#toucheventmanager-)
  - [`UserInputManager` #](#userinputmanager-)
- [構造体](#構造体)
  - [`JoystickAxis` #](#joystickaxis-)
  - [`Touch` #](#touch-)
- [列挙型](#列挙型)
  - [`ConfineMouseMode` #](#confinemousemode-)
  - [`FrameworkAction` #](#frameworkaction-)
  - [`JoystickAxisSource` #](#joystickaxissource-)
  - [`JoystickButton` #](#joystickbutton-)
  - [`MidiKey` #](#midikey-)
  - [`PlatformAction` #](#platformaction-)
  - [`TabletAuxiliaryButton` #](#tabletauxiliarybutton-)
  - [`TabletPenButton` #](#tabletpenbutton-)
  - [`TouchSource` #](#touchsource-)

# インターフェース
## `IHandleGlobalKeyboardInput` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/IHandleGlobalKeyboardInput.cs#L9)
```csharp
public interface IHandleGlobalKeyboardInput
```

## `IRequireHighFrequencyMousePosition` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/IRequireHighFrequencyMousePosition.cs#L12)
```csharp
public interface IRequireHighFrequencyMousePosition : IDrawable
```

## `ISourceGeneratedHandleInputCache` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/ISourceGeneratedHandleInputCache.cs#L8)
```csharp
public interface ISourceGeneratedHandleInputCache
```

## `ISuppressKeyEventLogging` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/ISuppressKeyEventLogging.cs#L10)
```csharp
public interface ISuppressKeyEventLogging
```

# クラス
## `ButtonEventManager<TButton>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/ButtonEventManager.cs#L18)
```csharp
public abstract class ButtonEventManager<TButton>
```

## `CustomInputManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/CustomInputManager.cs#L13)
```csharp
public partial class CustomInputManager : InputManager
```

## `InputManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/InputManager.cs#L34)
```csharp
public abstract partial class InputManager : Container, IInputStateChangeHandler
```

## `InputResampler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/InputResampler.cs#L15)
```csharp
public class InputResampler
```

## `JoystickAxisEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/JoystickAxisEventManager.cs#L17)
```csharp
public class JoystickAxisEventManager
```

## `JoystickButtonEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/JoystickButtonEventManager.cs#L11)
```csharp
public class JoystickButtonEventManager : ButtonEventManager<JoystickButton>
```

## `KeyEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/KeyEventManager.cs#L17)
```csharp
public class KeyEventManager : ButtonEventManager<Key>
```

## `MidiKeyEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/MidiKeyEventManager.cs#L11)
```csharp
public class MidiKeyEventManager : ButtonEventManager<MidiKey>
```

## `MouseButtonEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/MouseButtonEventManager.cs#L22)
```csharp
public abstract class MouseButtonEventManager : ButtonEventManager<MouseButton>
```

## `PassThroughInputManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/PassThroughInputManager.cs#L29)
```csharp
public partial class PassThroughInputManager : CustomInputManager, IRequireHighFrequencyMousePosition
```

## `PlatformActionContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/PlatformActionContainer.cs#L17)
```csharp
public partial class PlatformActionContainer : KeyBindingContainer<PlatformAction>, IHandleGlobalKeyboardInput
```

## `ReadableKeyCombinationProvider` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/ReadableKeyCombinationProvider.cs#L13)
```csharp
public class ReadableKeyCombinationProvider
```

## `TabletAuxiliaryButtonEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TabletAuxiliaryButtonEventManager.cs#L11)
```csharp
public class TabletAuxiliaryButtonEventManager : ButtonEventManager<TabletAuxiliaryButton>
```

## `TabletPenButtonEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TabletPenButtonEventManager.cs#L11)
```csharp
public class TabletPenButtonEventManager : ButtonEventManager<TabletPenButton>
```

## `TextInputSource` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TextInputSource.cs#L16)
```csharp
public class TextInputSource
```

## `TouchEventManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TouchEventManager.cs#L18)
```csharp
public class TouchEventManager : ButtonEventManager<TouchSource>
```

## `UserInputManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/UserInputManager.cs#L20)
```csharp
public partial class UserInputManager : PassThroughInputManager
```




# 構造体
## `JoystickAxis` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/JoystickAxis.cs#L6)
```csharp
public readonly struct JoystickAxis
```

## `Touch` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Touch.cs#L14)
```csharp
public readonly struct Touch : IEquatable<Touch>
```


# 列挙型
## `ConfineMouseMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/ConfineMouseMode.cs#L6)
```csharp
public enum ConfineMouseMode
```

## `FrameworkAction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/FrameworkActionContainer.cs#L33)
```csharp
public enum FrameworkAction
```

## `JoystickAxisSource` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/JoystickAxisSource.cs#L6)
```csharp
public enum JoystickAxisSource
```

## `JoystickButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/JoystickButton.cs#L6)
```csharp
public enum JoystickButton
```

## `MidiKey` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/MidiKey.cs#L6)
```csharp
public enum MidiKey
```

## `PlatformAction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/PlatformAction.cs#L6)
```csharp
public enum PlatformAction
```

## `TabletAuxiliaryButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TabletAuxiliaryButton.cs#L6)
```csharp
public enum TabletAuxiliaryButton
```

## `TabletPenButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TabletPenButton.cs#L6)
```csharp
public enum TabletPenButton
```

## `TouchSource` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/TouchSource.cs#L9)
```csharp
public enum TouchSource
```