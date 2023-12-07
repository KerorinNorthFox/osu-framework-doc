# osu.Framework.Graphics.Rendering.Vertices Doc
- [osu.Framework.Graphics.Rendering.Vertices Doc](#osuframeworkgraphicsrenderingvertices-doc)
- [インターフェース](#インターフェース)
  - [`IVertex` #](#ivertex-)
- [クラス](#クラス)
  - [`VertexMemberAttribute` #](#vertexmemberattribute-)
- [構造体](#構造体)
  - [`ParticleVertex2D` #](#particlevertex2d-)
  - [`TexturedVertex2D` #](#texturedvertex2d-)
  - [`TexturedVertex3D` #](#texturedvertex3d-)
  - [`TimedTexturedVertex2D` #](#timedtexturedvertex2d-)
  - [`UncolouredVertex2D` #](#uncolouredvertex2d-)
  - [`Vertex2D` #](#vertex2d-)

# インターフェース
## `IVertex` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/IVertex.cs#L6)
```csharp
public interface IVertex
```

# クラス
## `VertexMemberAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/VertexMemberAttribute.cs#L10)
```csharp
[AttributeUsage(AttributeTargets.Field)]
public class VertexMemberAttribute : Attribute
```

# 構造体
## `ParticleVertex2D` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/ParticleVertex2D.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct ParticleVertex2D : IEquatable<ParticleVertex2D>, IVertex
```

## `TexturedVertex2D` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/TexturedVertex2D.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct TexturedVertex2D : IEquatable<TexturedVertex2D>, IVertex
```

## `TexturedVertex3D` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/TexturedVertex3D.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct TexturedVertex3D : IEquatable<TexturedVertex3D>, IVertex
```

## `TimedTexturedVertex2D` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/TimedTexturedVertex2D.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct TimedTexturedVertex2D : IEquatable<TimedTexturedVertex2D>, IVertex
```

## `UncolouredVertex2D` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/UncolouredVertex2D.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct UncolouredVertex2D : IEquatable<UncolouredVertex2D>, IVertex
```

## `Vertex2D` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Rendering/Vertices/Vertex2D.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct Vertex2D : IEquatable<Vertex2D>, IVertex
```


