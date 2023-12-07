# osu.Framework.Graphics.Rendering Doc
- [osu.Framework.Graphics.Rendering Doc](#osuframeworkgraphicsrendering-doc)
- [インターフェース](#インターフェース)
  - [`IFrameBuffer` #](#iframebuffer-)
  - [`INativeTexture` #](#inativetexture-)
  - [`IRenderer` #](#irenderer-)
  - [`IShaderPart` #](#ishaderpart-)
  - [`IShaderStorageBufferObject<TData>` #](#ishaderstoragebufferobjecttdata-)
  - [`IUniformBuffer` #](#iuniformbuffer-)
  - [`IUniformBuffer<TData>` #](#iuniformbuffertdata-)
  - [`IVertexBatch` #](#ivertexbatch-)
  - [`IVertexBatch<in TVertex>` #](#ivertexbatchin-tvertex-)
- [クラス](#クラス)
  - [`DepthValue` #](#depthvalue-)
  - [`Renderer` #](#renderer-)
  - [`RendererExtensions` #](#rendererextensions-)
  - [`ShaderStorageBufferObjectStack` #](#shaderstoragebufferobjectstack-)
- [構造体](#構造体)
  - [`ClearInfo` #](#clearinfo-)
  - [`DepthInfo` #](#depthinfo-)
  - [`GlobalUniformData` #](#globaluniformdata-)
  - [`MaskingInfo` #](#maskinginfo-)
  - [`StencilInfo` #](#stencilinfo-)
- [列挙型](#列挙型)
  - [`BufferTestFunction` #](#buffertestfunction-)
  - [`FlushBatchSource` #](#flushbatchsource-)
  - [`PrimitiveTopology` #](#primitivetopology-)
  - [`RenderBufferFormat` #](#renderbufferformat-)
  - [`StencilOperation` #](#stenciloperation-)

# インターフェース
## `IFrameBuffer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IFrameBuffer.cs#L10)
```csharp
public interface IFrameBuffer : IDisposable
```

## `INativeTexture` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/INativeTexture.cs#L10)
```csharp
public interface INativeTexture : IDisposable
```

## `IRenderer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IRenderer.cs#L21)
```csharp
public interface IRenderer
```

## `IShaderPart` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IShaderPart.cs#L8)
```csharp
public interface IShaderPart : IDisposable
```

## `IShaderStorageBufferObject<TData>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IShaderStorageBufferObject.cs#L12)
```csharp
public interface IShaderStorageBufferObject<TData> : IUniformBuffer
    where TData : unmanaged, IEquatable<TData>
```

## `IUniformBuffer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IUniformBuffer.cs#L11)
```csharp
public interface IUniformBuffer : IDisposable
```

## `IUniformBuffer<TData>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IUniformBuffer.cs#L17)
```csharp
public interface IUniformBuffer<TData> : IUniformBuffer
    where TData : unmanaged, IEquatable<TData>
```

## `IVertexBatch` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IVertexBatch.cs#L9)
```csharp
public interface IVertexBatch : IDisposable
```

## `IVertexBatch<in TVertex>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/IVertexBatch.cs#L25)
```csharp
public interface IVertexBatch<in TVertex> : IVertexBatch
    where TVertex : unmanaged, IEquatable<TVertex>, IVertex
```

# クラス
## `DepthValue` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/DepthValue.cs#L12)
```csharp
public class DepthValue
```

## `Renderer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Renderer.cs#L35)
```csharp
public abstract class Renderer : IRenderer
```

## `RendererExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/RendererExtensions.cs#L17)
```csharp
public static class RendererExtensions
```

## `ShaderStorageBufferObjectStack` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/ShaderStorageBufferObjectStack.cs#L13)
```csharp
public class ShaderStorageBufferObjectStack<TData> : IDisposable
    where TData : unmanaged, IEquatable<TData>
```


# 構造体
## `ClearInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/ClearInfo.cs#L11)
```csharp
public readonly struct ClearInfo
```

## `DepthInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/DepthInfo.cs#L11)
```csharp
public readonly struct DepthInfo : IEquatable<DepthInfo>
```

## `GlobalUniformData` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/GlobalUniformData.cs#L11)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1)]
public record struct GlobalUniformData
```

## `MaskingInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/MaskingInfo.cs#L11)
```csharp
public struct MaskingInfo : IEquatable<MaskingInfo>
```

## `StencilInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/StencilInfo.cs#L8)
```csharp
public readonly struct StencilInfo : IEquatable<StencilInfo>
```


# 列挙型
## `BufferTestFunction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/BufferTestFunction.cs#L6)
```csharp
public enum BufferTestFunction
```

## `FlushBatchSource` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/FlushBatchSource.cs#L6)
```csharp
public enum FlushBatchSource
```

## `PrimitiveTopology` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/PrimitiveTopology.cs#L6)
```csharp
public enum PrimitiveTopology
```

## `RenderBufferFormat` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/RenderBufferFormat.cs#L6)
```csharp
public enum RenderBufferFormat
```

## `StencilOperation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/StencilOperation.cs#L6)
```csharp
public enum StencilOperation
```
