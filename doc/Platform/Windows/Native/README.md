# osu.Framework.Platform.Windows.Native Doc
- [osu.Framework.Platform.Windows.Native Doc](#osuframeworkplatformwindowsnative-doc)
- [構造体](#構造体)
  - [`RawInputData` #](#rawinputdata-)
  - [`RawMouse` #](#rawmouse-)
  - [`RawInputHeader` #](#rawinputheader-)
  - [`RawInputDevice` #](#rawinputdevice-)
- [列挙型](#列挙型)
  - [`RawMouseFlags` #](#rawmouseflags-)
  - [`RawMouseButtons` #](#rawmousebuttons-)
  - [`RawInputCommand` #](#rawinputcommand-)
  - [`RawInputType` #](#rawinputtype-)
  - [`RawInputDeviceFlags` #](#rawinputdeviceflags-)
  - [`HIDUsage` #](#hidusage-)
  - [`HIDUsagePage` #](#hidusagepage-)
  - [`FeedbackType` #](#feedbacktype-)

# 構造体
## `RawInputData` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L85)
```csharp
public struct RawInputData
```

## `RawMouse` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L99)
```csharp
public struct RawMouse
```

## `RawInputHeader` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L246)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct RawInputHeader
```

## `RawInputDevice` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L262)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct RawInputDevice
```


# 列挙型
## `RawMouseFlags` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L143)
```csharp
[Flags]
public enum RawMouseFlags : ushort
```

## `RawMouseButtons` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L164)
```csharp
public enum RawMouseButtons : ushort
```

## `RawInputCommand` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L206)
```csharp
public enum RawInputCommand
```

## `RawInputType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L222)
```csharp
public enum RawInputType
```

## `RawInputDeviceFlags` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L280)
```csharp
public enum RawInputDeviceFlags
```

## `HIDUsage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L310)
```csharp
public enum HIDUsage
```

## `HIDUsagePage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L321)
```csharp
public enum HIDUsagePage
```

## `FeedbackType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Platform/Windows/Native/Input.cs#L353)
```csharp
public enum FeedbackType
```