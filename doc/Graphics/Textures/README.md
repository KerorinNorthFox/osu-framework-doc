# osu.Framework.Graphics.Textures Doc
- [osu.Framework.Graphics.Textures Doc](#osuframeworkgraphicstextures-doc)
- [インターフェース](#インターフェース)
  - [`ITextureStore` #](#itexturestore-)
  - [`ITextureUpload` #](#itextureupload-)
- [クラス](#クラス)
  - [`ArrayPoolTextureUpload` #](#arraypooltextureupload-)
  - [`DisposableTexture` #](#disposabletexture-)
  - [`LargeTextureStore` #](#largetexturestore-)
  - [`MemoryAllocatorTextureUpload` #](#memoryallocatortextureupload-)
  - [`Texture` #](#texture-)
  - [`TextureAtlas` #](#textureatlas-)
  - [`TextureAtlas` #](#textureatlas--1)
  - [`TextureLoaderStore` #](#textureloaderstore-)
  - [`TextureRegion` #](#textureregion-)
  - [`TextureStore` #](#texturestore-)
  - [`TextureTooLargeForGLException` #](#texturetoolargeforglexception-)
  - [`TextureUpload` #](#textureupload-)
- [列挙型](#列挙型)
  - [`Opacity` #](#opacity-)
  - [`TextureFilteringMode` #](#texturefilteringmode-)
  - [`WrapMode` #](#wrapmode-)

# インターフェース
## `ITextureStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/ITextureStore.cs#L13)
```csharp
public interface ITextureStore : IResourceStore<Texture>
```

## `ITextureUpload` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/ITextureUpload.cs#L11)
```csharp
public interface ITextureUpload : IDisposable
```

# クラス
## `ArrayPoolTextureUpload` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/ArrayPoolTextureUpload.cs#L14)
```csharp
public class ArrayPoolTextureUpload : ITextureUpload
```

## `DisposableTexture` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/DisposableTexture.cs#L11)
```csharp
public class DisposableTexture : Texture
```

## `LargeTextureStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/LargeTextureStore.cs#L22)
```csharp
public class LargeTextureStore : TextureStore
```

## `MemoryAllocatorTextureUpload` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/MemoryAllocatorTextureUpload.cs#L15)
```csharp
public class MemoryAllocatorTextureUpload : ITextureUpload
```

## `Texture` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/Texture.cs#L14)
```csharp
public class Texture : IDisposable
```

## `TextureAtlas` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureAtlas.cs#L17)
```csharp
public partial class TextureAtlas
```

## `TextureAtlas` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureAtlas_BackingAtlasTexture.cs#L13)
```csharp
public partial class TextureAtlas
```

## `TextureLoaderStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureLoaderStore.cs#L20)
```csharp
public class TextureLoaderStore : IResourceStore<TextureUpload>
```

## `TextureRegion` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureRegion.cs#L12)
```csharp
public class TextureRegion : Texture
```

## `TextureStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureStore.cs#L24)
```csharp
public class TextureStore : ITextureStore
```

## `TextureTooLargeForGLException` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureTooLargeForGLException.cs#L8)
```csharp
public class TextureTooLargeForGLException : InvalidOperationException
```

## `TextureUpload` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureUpload.cs#L25)
```csharp
public class TextureUpload : ITextureUpload
```




# 列挙型
## `Opacity` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/Opacity.cs#L6)
```csharp
public enum Opacity
```

## `TextureFilteringMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/TextureFilteringMode.cs#L6)
```csharp
public enum TextureFilteringMode
```

## `WrapMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/WrapMode.cs#L6)
```csharp
public enum WrapMode
```