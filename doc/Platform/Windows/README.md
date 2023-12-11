# osu.Framework.Platform.Windows Doc
- [osu.Framework.Platform.Windows Doc](#osuframeworkplatformwindows-doc)
- [インターフェース](#インターフェース)
  - [`IWindowsRenderer` #](#iwindowsrenderer-)
- [クラス](#クラス)
  - [`WindowsClipboard` #](#windowsclipboard-)
  - [`WindowsGameHost` #](#windowsgamehost-)
  - [`WindowsReadableKeyCombinationProvider` #](#windowsreadablekeycombinationprovider-)
- [列挙型](#列挙型)
  - [`FullscreenCapability` #](#fullscreencapability-)

# インターフェース
## `IWindowsRenderer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/IWindowsRenderer.cs#L8)
```csharp
public interface IWindowsRenderer
```

# クラス
## `WindowsClipboard` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/WindowsClipboard.cs#L15)
```csharp
public class WindowsClipboard : Clipboard
```

## `WindowsGameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/WindowsGameHost.cs#L21)
```csharp
[SupportedOSPlatform("windows")]
public class WindowsGameHost : DesktopGameHost
```

## `WindowsReadableKeyCombinationProvider` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/WindowsReadableKeyCombinationProvider.cs#L10)
```csharp
public class WindowsReadableKeyCombinationProvider : SDL2ReadableKeyCombinationProvider
```



# 列挙型
## `FullscreenCapability` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/FullscreenCapability.cs#L6)
```csharp
public enum FullscreenCapability
```