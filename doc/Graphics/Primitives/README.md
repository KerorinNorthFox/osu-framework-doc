# osu.Framework.Graphics.Primitives Doc
- [osu.Framework.Graphics.Primitives Doc](#osuframeworkgraphicsprimitives-doc)
- [インターフェース](#インターフェース)
  - [`IConvexPolygon` #](#iconvexpolygon-)
  - [`IPolygon` #](#ipolygon-)
- [クラス](#クラス)
  - [`SimpleConvexPolygon` #](#simpleconvexpolygon-)
- [構造体](#構造体)
  - [`Line` #](#line-)
  - [`Quad` #](#quad-)
  - [`RectangleF` #](#rectanglef-)
  - [`RectangleI` #](#rectanglei-)
  - [`Triangle` #](#triangle-)
  - [`Vector2I` #](#vector2i-)

# インターフェース
## `IConvexPolygon` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/IConvexPolygon.cs#L6)
```csharp
public interface IConvexPolygon : IPolygon
```

## `IPolygon` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/IPolygon.cs#L9)
```csharp
public interface IPolygon
```

# クラス
## `SimpleConvexPolygon` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/SimpleConvexPolygon.cs#L10)
```csharp
public class SimpleConvexPolygon : IConvexPolygon
```

# 構造体
## `Line` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/Line.cs#L14)
```csharp
public readonly struct Line
```

## `Quad` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/Quad.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential)]
public readonly struct Quad : IConvexPolygon, IEquatable<Quad>
```

## `RectangleF` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/RectangleF.cs#L18)
```csharp
[Serializable, StructLayout(LayoutKind.Sequential)]
public struct RectangleF : IEquatable<RectangleF>
```

## `RectangleI` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/RectangleI.cs#L18)
```csharp
[Serializable, StructLayout(LayoutKind.Sequential)]
public struct RectangleI : IEquatable<RectangleI>
```

## `Triangle` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/Triangle.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential)]
public readonly struct Triangle : IConvexPolygon, IEquatable<Triangle>
```

## `Vector2I` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Primitives/Vector2I.cs#L14)
```csharp
[Serializable, StructLayout(LayoutKind.Sequential)]
public struct Vector2I : IEquatable<Vector2I>
```