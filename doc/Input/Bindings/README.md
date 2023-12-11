# osu.Framework.Input.Bindings Doc
- [osu.Framework.Input.Bindings Doc](#osuframeworkinputbindings-doc)
- [インターフェース](#インターフェース)
  - [`IKeyBinding` #](#ikeybinding-)
  - [`IKeyBindingHandler<T>` #](#ikeybindinghandlert-)
  - [`IKeyBindingHandler` #](#ikeybindinghandler-)
  - [`IScrollBindingHandler<T>` #](#iscrollbindinghandlert-)
  - [`KeyBinding` #](#keybinding-)
  - [`KeyBindingContainer<T>` #](#keybindingcontainert-)
  - [`KeyBindingContainer` #](#keybindingcontainer-)
  - [`KeyBindingExtensions` #](#keybindingextensions-)
- [構造体](#構造体)
  - [`KeyCombination` #](#keycombination-)
- [列挙型](#列挙型)
  - [`InputKey` #](#inputkey-)
  - [`SimultaneousBindingMode` #](#simultaneousbindingmode-)
  - [`KeyCombinationMatchingMode` #](#keycombinationmatchingmode-)

# インターフェース
## `IKeyBinding` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/IKeyBinding.cs#L9)
```csharp
public interface IKeyBinding
```

## `IKeyBindingHandler<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/IKeyBindingHandler.cs#L13)
```csharp
public interface IKeyBindingHandler<T> : IKeyBindingHandler
    where T : struct
```

## `IKeyBindingHandler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/IKeyBindingHandler.cs#L31)
```csharp
public interface IKeyBindingHandler : IDrawable
```

## `IScrollBindingHandler<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/IScrollBindingHandler.cs#L12)
```csharp
public interface IScrollBindingHandler<T> : IKeyBindingHandler<T>
    where T : struct
```

## `KeyBinding` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyBinding.cs#L8)
```csharp
public class KeyBinding : IKeyBinding
```

## `KeyBindingContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyBindingContainer.cs#L22)
```csharp
public abstract partial class KeyBindingContainer<T> : KeyBindingContainer
    where T : struct
```

## `KeyBindingContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyBindingContainer.cs#L424)
```csharp
public abstract partial class KeyBindingContainer : Container
```

## `KeyBindingExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyBindingExtensions.cs#L6)
```csharp
public static class KeyBindingExtensions
```

# 構造体
## `KeyCombination` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyCombination.cs#L19)
```csharp
public readonly struct KeyCombination : IEquatable<KeyCombination>
```



# 列挙型
## `InputKey` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/InputKey.cs#L12)
```csharp
public enum InputKey
```

## `SimultaneousBindingMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyBindingContainer.cs#L452)
```csharp
public enum SimultaneousBindingMode
```

## `KeyCombinationMatchingMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Bindings/KeyCombination.cs#L19C5-L19C71#L651)
```csharp
public enum KeyCombinationMatchingMode
```