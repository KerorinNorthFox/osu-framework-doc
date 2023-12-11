# osu.Framework.Graphics Doc
- [osu.Framework.Graphics Doc](#osuframeworkgraphics-doc)
- [インターフェース](#インターフェース)
  - [`IBufferedDrawable` #](#ibuffereddrawable-)
  - [`ICompositeDrawNode` #](#icompositedrawnode-)
  - [`IDrawable` #](#idrawable-)
  - [`ITexturedShaderDrawable` #](#itexturedshaderdrawable-)
- [クラス](#クラス)
  - [`BufferedDrawNode` #](#buffereddrawnode-)
  - [`BufferedDrawNodeSharedData` #](#buffereddrawnodeshareddata-)
  - [`Component` #](#component-)
  - [`DrawableExtensions` #](#drawableextensions-)
  - [`Drawable` #](#drawable-)
  - [`Drawable` #](#drawable--1)
  - [`Drawable` #](#drawable--2)
  - [`FrameworkColour` #](#frameworkcolour-)
  - [`FrameworkFont` #](#frameworkfont-)
  - [`TexturedShaderDrawNode` #](#texturedshaderdrawnode-)
  - [`TransformSequenceExtensions` #](#transformsequenceextensions-)
  - [`TransformableExtensions` #](#transformableextensions-)
  - [`Vector2Extensions` #](#vector2extensions-)
- [構造体](#構造体)
  - [`BlendingParameters` #](#blendingparameters-)
  - [`Colour4` #](#colour4-)
  - [`DrawColourInfo` #](#drawcolourinfo-)
  - [`DrawInfo` #](#drawinfo-)
  - [`DrawNode` #](#drawnode-)
  - [`Drawable` #](#drawable--3)
  - [`MarginPadding` #](#marginpadding-)
- [列挙型](#列挙型)
  - [`BlendingEquation` #](#blendingequation-)
  - [`BlendingMask` #](#blendingmask-)
  - [`BlendingType` #](#blendingtype-)
  - [`Invalidation` #](#invalidation-)
  - [`Anchor` #](#anchor-)
  - [`Axes` #](#axes-)
  - [`Edges` #](#edges-)
  - [`Direction` #](#direction-)
  - [`RotationDirection` #](#rotationdirection-)
  - [`LoadState` #](#loadstate-)
  - [`FillMode` #](#fillmode-)
  - [`Easing` #](#easing-)

# インターフェース
## `IBufferedDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/IBufferedDrawable.cs#L13)
```csharp
public interface IBufferedDrawable : ITexturedShaderDrawable
```

## `ICompositeDrawNode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/ICompositeDrawNode.cs#L13)
```csharp
public interface ICompositeDrawNode
```

## `IDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/IDrawable.cs#L19)
```csharp
public interface IDrawable : ITransformable
```

## `ITexturedShaderDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/ITexturedShaderDrawable.cs#L11)
```csharp
public interface ITexturedShaderDrawable : IDrawable
```




# クラス
## `BufferedDrawNode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/BufferedDrawNode.cs#L16)
```csharp
public class BufferedDrawNode : TexturedShaderDrawNode
```

## `BufferedDrawNodeSharedData` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/BufferedDrawNodeSharedData.cs#L19)
```csharp
public class BufferedDrawNodeSharedData : IDisposable
```

## `Component` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Component.cs#L11)
```csharp
public abstract partial class Component : Drawable
```

## `DrawableExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/DrawableExtensions.cs#L14)
```csharp
public static class DrawableExtensions
```

## `Drawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable_HandleInputCache.cs#L14)
```csharp
public partial class Drawable
```

## `Drawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable_IsLongRunning.cs#L9)
```csharp
public partial class Drawable
```

## `Drawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable_ProxyDrawable.cs#L11)
```csharp
public partial class Drawable
```

## `FrameworkColour` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/FrameworkColour.cs#L8)
```csharp
public static class FrameworksColour
```

## `FrameworkFont` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/FrameworkFont.cs#L8)
```csharp
public static class FrameworkFont
```

## `TexturedShaderDrawNode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/TexturedShaderDrawNode.cs#L11)
```csharp
public abstract class TexturedShaderDrawNode : DrawNode
```

## `TransformSequenceExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/TransformSequenceExtensions.cs#L15)
```csharp
public static class TransformSequenceExtensions
```

## `TransformableExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/TransformableExtensions.cs#L20)
```csharp
public static class TransformableExtensions
```

## `Vector2Extensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Vector2Extensions.cs#L11)
```csharp
public static class Vector2Extensions
```




# 構造体
## `BlendingParameters` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/BlendingParameters.cs#L15)
```csharp
public struct BlendingParameters : IEquatable<BlendingParameters>
```

## `Colour4` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Colour4.cs#L17)
```csharp
public readonly struct Colour4 : IEquatable<Colour4>
```

## `DrawColourInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/DrawColourInfo.cs#L10)
```csharp
public struct DrawColourInfo : IEquatable<DrawColourInfo>
```

## `DrawInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/DrawInfo.cs#L12)
```csharp
public struct DrawInfo : IEquatable<DrawInfo>
```

## `DrawNode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/DrawNode.cs#L16)
```csharp
public class DrawNode : IDisposable
```

## `Drawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L53)
```csharp
public abstract partial class Drawable : Transformable, IDisposable, IDrawable
```

## `MarginPadding` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/MarginPadding.cs#L15)
```csharp
public struct MarginPadding : IInterpolable<MarginPadding>, IEquatable<MarginPadding>
```



# 列挙型
## `BlendingEquation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/BlendingEquation.cs#L6)
```csharp
public enum BlendingEquation
```

## `BlendingMask` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/BlendingMask.cs#L13)
```csharp
[Flags]
public enum BlendingMask
```

## `BlendingType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/BlendingType.cs#L6)
```csharp
public enum BlendingType
```

## `Invalidation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2606)
```csharp
[Flag]
public enum Invalidation
```

## `Anchor` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2673)
```csharp
[Flags]
public enum Anchor
```

## `Axes` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2724)
```csharp
[Flags]
public enum Axes
```

## `Edges` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2735)
```csharp
[Flags]
public enum Edges
```

## `Direction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L22750)
```csharp
public enum Direction
```

## `RotationDirection` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2756)
```csharp
public enum RotationDirection
```

## `LoadState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2768)
```csharp
public enum LoadState
```

## `FillMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Drawable.cs#L2796)
```csharp
public enum FillMode
```

## `Easing` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Easing.cs#L9)
```csharp
public enum Easing
```