# osu.Framework.Screens Doc
- [osu.Framework.Screens Doc](#osuframeworkscreens-doc)
- [インターフェース](#インターフェース)
  - [`IScreen` #](#iscreen-)
- [クラス](#クラス)
  - [`ScreenExtensions` #](#screenextensions-)
  - [`Screen` #](#screen-)
  - [`ScreenExitEvent` #](#screenexitevent-)
  - [`ScreenStack` #](#screenstack-)
  - [`ScreenTransitionEvent` #](#screentransitionevent-)
- [デリゲート](#デリゲート)
  - [`ScreenChangedDelegate` #](#screenchangeddelegate-)

# インターフェース
## `IScreen` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/IScreen.cs#L11)
```csharp
public interface IScreen : IDrawable
```

# クラス
## `ScreenExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/IScreen.cs#L49)
```csharp
public static class ScreenExtensions
```

## `Screen` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/Screen.cs#L12)
```csharp
public partial class Screen : CompositeDrawable, IScreen
```

## `ScreenExitEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/ScreenExitEvent.cs#L9)
```csharp
public class ScreenExitEvent : ScreenTransitionEvent
```

## `ScreenStack` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/ScreenStack.cs#L22)
```csharp
public partial class ScreenStack : CompositeDrawable
```

## `ScreenTransitionEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/ScreenTransitionEvent.cs#L9)
```csharp
public class ScreenTransitionEvent
```

# デリゲート
## `ScreenChangedDelegate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Screens/ScreenStack.cs#L468)
```csharp
public delegate void ScreenChangedDelegate(IScreen lastScreen, IScreen newScreen);
```