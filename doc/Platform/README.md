# osu.Framework.Platform Doc
- [osu.Framework.Platform Doc](#osuframeworkplatform-doc)
- [インターフェース](#インターフェース)
  - [`IGraphicsSurface` #](#igraphicssurface-)
  - [`IIpcHost` #](#iipchost-)
  - [`ILinuxGraphicsSurface` #](#ilinuxgraphicssurface-)
  - [`IMetalGraphicsSurface` #](#imetalgraphicssurface-)
  - [`IOpenGLGraphicsSurface` #](#iopenglgraphicssurface-)
  - [`IWindow` #](#iwindow-)
- [クラス](#クラス)
  - [`Clipboard` #](#clipboard-)
  - [`DesktopGameHost` #](#desktopgamehost-)
  - [`DesktopStorage` #](#desktopstorage-)
  - [`Display` #](#display-)
  - [`FlushingStream` #](#flushingstream-)
  - [`GameHost` #](#gamehost-)
  - [`HeadlessClipboard` #](#headlessclipboard-)
  - [`HeadlessGameHost` #](#headlessgamehost-)
  - [`IpcChannel<T>` #](#ipcchannelt-)
  - [`IpcMessage` #](#ipcmessage-)
  - [`MonoPInvokeCallbackAttribute` #](#monopinvokecallbackattribute-)
  - [`NativeMemoryTracker` #](#nativememorytracker-)
  - [`NativeStorage` #](#nativestorage-)
  - [`OsuTKGameHost` #](#osutkgamehost-)
  - [`SDL2GameHost` #](#sdl2gamehost-)
  - [`Storage` #](#storage-)
  - [`TcpIpcProvider` #](#tcpipcprovider-)
  - [`ThreadRunner` #](#threadrunner-)
- [構造体](#構造体)
  - [`DisplayMode` #](#displaymode-)
- [列挙型](#列挙型)
  - [`ExecutionMode` #](#executionmode-)
  - [`ExecutionState` #](#executionstate-)
  - [`GraphicsSurfaceType` #](#graphicssurfacetype-)
  - [`CursorState` #](#cursorstate-)
  - [`WindowState` #](#windowstate-)

# インターフェース
## `IGraphicsSurface` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IGraphicsSurface.cs#L12)
```csharp
public interface IGraphicsSurface
```

## `IIpcHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IIpcHost.cs#L9)
```csharp
public interface IIpcHost
```

## `ILinuxGraphicsSurface` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/ILinuxGraphicsSurface.cs#L6)
```csharp
public interface ILinuxGraphicsSurface
```

## `IMetalGraphicsSurface` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IMetalGraphicsSurface.cs#L11)
```csharp
public interface IMetalGraphicsSurface
```

## `IOpenGLGraphicsSurface` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IOpenGLGraphicsSurface.cs#L11)
```csharp
public interface IOpenGLGraphicsSurface
```

## `IWindow` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IWindow.cs#L17)
```csharp
public interface IWindow : IDisposable
```




# クラス
## `Clipboard` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Clipboard.cs#L12)
```csharp
public abstract class Clipboard
```

## `DesktopGameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/DesktopGameHost.cs#L16)
```csharp
public abstract class DesktopGameHost : SDL2GameHost
```

## `DesktopStorage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/DesktopStorage.cs#L6)
```csharp
public class DesktopStorage : NativeStorage
```

## `Display` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Display.cs#L13)
```csharp
public sealed class Display : IEquatable<Display>
```

## `FlushingStream` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/FlushingStream.cs#L15)
```csharp
public class FlushingStream : FileStream
```

## `GameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/GameHost.cs#L52)
```csharp
public abstract class GameHost : IIpcHost, IDisposable
```

## `HeadlessClipboard` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/HeadlessClipboard.cs#L14)
```csharp
public class HeadlessClipboard : Clipboard
```

## `HeadlessGameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/HeadlessGameHost.cs#L19)
```csharp
public class HeadlessGameHost : DesktopGameHost
```

## `IpcChannel<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IpcChannel.cs#L11)
```csharp
public class IpcChannel<T> : IDisposable
```

## `IpcMessage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/IpcMessage.cs#L8)
```csharp
public class IpcMessage
```

## `MonoPInvokeCallbackAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/MonoPInvokeCallbackAttribute.cs#L10)
```csharp
[AttributeUsage(AttributeTargets.Method)]
public sealed class MonoPInvokeCallbackAttribute : Attribute
```

## `NativeMemoryTracker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/NativeMemoryTracker.cs#L14)
```csharp
public static class NativeMemoryTracker
```

## `NativeStorage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/NativeStorage.cs#L16)
```csharp
public class NativeStorage : Storage
```

## `OsuTKGameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/OsuTKGameHost.cs#L11)
```csharp
public abstract class OsuTKGameHost : GameHost
```

## `SDL2GameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/SDL2GameHost.cs#L17)
```csharp
public abstract class SDL2GameHost : GameHost
```

## `Storage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Storage.cs#L14)
```csharp
public abstract class Storage
```

## `TcpIpcProvider` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/TcpIpcProvider.cs#L22)
```csharp
public class TcpIpcProvider : IDisposable
```

## `ThreadRunner` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/ThreadRunner.cs#L22)
```csharp
public class ThreadRunner
```



# 構造体
## `DisplayMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/DisplayMode.cs#L12)
```csharp
public readonly struct DisplayMode : IEquatable<DisplayMode>
```



# 列挙型
## `ExecutionMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/ExecutionMode.cs#L8)
```csharp
public enum ExecutionMode
```

## `ExecutionState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/GameHost.cs#L1487)
```csharp
public enum ExecutionState
```

## `GraphicsSurfaceType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/GraphicsSurfaceType.cs#L11)
```csharp
public enum GraphicsSurfaceType
```

## `CursorState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/OsuTKWindow.cs#L590)
```csharp
[Flags]
public enum CursorState
```

## `WindowState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/WindowState.cs#L9)
```csharp
public enum WindowState
```