# osu.Framework.Graphics.Textures Doc

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

# 列挙型
## `Opacity` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Textures/Opacity.cs#L6)
```csharp
public enum Opacity
```