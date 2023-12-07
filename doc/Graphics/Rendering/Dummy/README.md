# osu.Framework.Graphics.Rendering.Dummy Doc
- [osu.Framework.Graphics.Rendering.Dummy Doc](#osuframeworkgraphicsrenderingdummy-doc)
- [クラス](#クラス)
  - [`DummyRenderer` #](#dummyrenderer-)
  - [`DummyShaderStorageBufferObject<T>` #](#dummyshaderstoragebufferobjectt-)

# クラス
## `DummyRenderer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Dummy/DummyRenderer.cs#L22)
```csharp
public sealed class DummyRenderer : IRenderer
```

## `DummyShaderStorageBufferObject<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Dummy/DummyShaderStorageBufferObject.cs#L8)
```csharp
public class DummyShaderStorageBufferObject<T> : IShaderStorageBufferObject<T>
    where T : unmanaged, IEquatable<T>
```