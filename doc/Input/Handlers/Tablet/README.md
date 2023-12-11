# osu.Framework.Input.Handlers.Tablet Doc
- [osu.Framework.Input.Handlers.Tablet Doc](#osuframeworkinputhandlerstablet-doc)
- [インターフェース](#インターフェース)
  - [`ITabletHandler` #](#itablethandler-)
- [クラス](#クラス)
  - [`AbsoluteTabletMode` #](#absolutetabletmode-)
  - [`OpenTabletDriverHandler` #](#opentabletdriverhandler-)
  - [`TabletDriver` #](#tabletdriver-)
  - [`TabletInfo` #](#tabletinfo-)

# インターフェース
## `ITabletHandler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/Tablet/ITabletHandler.cs#L13)
```csharp
public interface ITabletHandler
```

# クラス
## `AbsoluteTabletMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/Tablet/AbsoluteTabletMode.cs#L9)
```csharp
public class AbsoluteTabletMode : AbsoluteOutputMode
```

## `OpenTabletDriverHandler` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/Tablet/OpenTabletDriverHandler.cs#L21)
```csharp
public class OpenTabletDriverHandler : InputHandler, IAbsolutePointer, IRelativePointer, IPressureHandler, ITabletHandler
```

## `TabletDriver` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/Tablet/TabletDriver.cs#L17)
```csharp
public sealed class TabletDriver : Driver
```

## `TabletInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Input/Handlers/Tablet/TabletInfo.cs#L12)
```csharp
public class TabletInfo
```