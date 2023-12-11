# osu.Framework.Graphics.Video Doc
- [osu.Framework.Graphics.Video Doc](#osuframeworkgraphicsvideo-doc)
- [クラス](#クラス)
  - [`DecodedFrame` #](#decodedframe-)
  - [`FFmpegCodec` #](#ffmpegcodec-)
  - [`FFmpegFuncs` #](#ffmpegfuncs-)
  - [`Video` #](#video-)
  - [`VideoDecoder` #](#videodecoder-)
  - [`VideoTextureUpload` #](#videotextureupload-)
- [列挙型](#列挙型)
  - [`HardwareVideoDecoder` #](#hardwarevideodecoder-)

# クラス
## `DecodedFrame` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/DecodedFrame.cs#L13)
```csharp
public class DecodedFrame
```

## `FFmpegCodec` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/FFmpegCodec.cs#L13)
```csharp
public sealed unsafe class FFmpegCodec
```

## `FFmpegFuncs` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/FFmpegFuncs.cs#L14)
```csharp
public unsafe class FFmpegFuncs
```

## `Video` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/Video.cs#L22)
```csharp
public partial class Video : AnimationClockComposite
```

## `VideoDecoder` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/VideoDecoder.cs#L33)
```csharp
public unsafe class VideoDecoder : IDisposable
```

## `VideoTextureUpload` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/VideoTextureUpload.cs#L13)
```csharp
public sealed unsafe class VideoTextureUpload : ITextureUpload
```


# 列挙型
## `HardwareVideoDecoder` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Video/HardwareVideoDecoder.cs#L16)
```csharp
[Flags]
public enum HardwareVideoDecoder
```