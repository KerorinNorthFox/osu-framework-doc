# osu.Framework.Input.Handlers Doc
- [osu.Framework.Input.Handlers Doc](#osuframeworkinputhandlers-doc)
- [インターフェース](#インターフェース)
  - [`IHasCursorSensitivity` #](#ihascursorsensitivity-)
  - [`INeedsMousePositionFeedback` #](#ineedsmousepositionfeedback-)
- [クラス](#クラス)
  - [`InputHandler` #](#inputhandler-)

# インターフェース
## `IHasCursorSensitivity` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/IHasCursorSensitivity.cs#L11)
```csharp
public interface IHasCursorSensitivity
```

## `INeedsMousePositionFeedback` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/INeedsMousePositionFeedback.cs#L11)
```csharp
public interface INeedsMousePositionFeedback
```

# クラス
## `InputHandler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/InputHandler.cs#L16)
```csharp
public abstract class InputHandler : IDisposable, IHasDescription
```