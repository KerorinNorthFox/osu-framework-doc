# osu.Framework.Extensions.ImageExtensions Doc
- [osu.Framework.Extensions.ImageExtensions Doc](#osuframeworkextensionsimageextensions-doc)
- [クラス](#クラス)
  - [`ImageExtensions` #](#imageextensions-)
- [構造体](#構造体)
  - [`ReadOnlyPixelMemory<TPixel>` #](#readonlypixelmemorytpixel-)
  - [`ReadOnlyPixelSpan<TPixel>` #](#readonlypixelspantpixel-)


# クラス
## `ImageExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Extensions/ImageExtensions/ImageExtensions.cs#L11)
```csharp
public static class ImageExtensions
```




# 構造体
## `ReadOnlyPixelMemory<TPixel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Extensions/ImageExtensions/ReadOnlyPixelMemory.cs#L12)
```csharp
public struct ReadOnlyPixelMemory<TPixel> : IDisposable
        where TPixel : unmanaged, IPixel<TPixel>
```

## `ReadOnlyPixelSpan<TPixel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Extensions/ImageExtensions/ReadOnlyPixelSpan.cs#L11)
```csharp
public readonly ref struct ReadOnlyPixelSpan<TPixel>
        where TPixel : unmanaged, IPixel<TPixel>
```
