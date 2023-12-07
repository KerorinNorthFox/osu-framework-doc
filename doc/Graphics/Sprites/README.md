# osu.Framework.Graphics.Sprites Doc
- [osu.Framework.Graphics.Sprites Doc](#osuframeworkgraphicssprites-doc)
- [インターフェース](#インターフェース)
  - [`IHasLineBaseHeight` #](#ihaslinebaseheight-)
  - [`IHasText` #](#ihastext-)
- [クラス](#クラス)
  - [`BufferedContainerView<T>` #](#bufferedcontainerviewt-)
  - [`FontAwesome` #](#fontawesome-)
  - [`Sprite` #](#sprite-)
  - [`SpriteDrawNode` #](#spritedrawnode-)
  - [`SpriteIcon` #](#spriteicon-)
  - [`SpriteText` #](#spritetext-)
  - [`SpriteText` #](#spritetext--1)
- [構造体](#構造体)
  - [`FontUsage` #](#fontusage-)
  - [`IconUsage` #](#iconusage-)

# インターフェース
## `IHasLineBaseHeight` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/IHasLineBaseHeight.cs#L9)
```csharp
public interface IHasLineBaseHeight
```

## `IHasText` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/IHasText.cs#L11)
```csharp
public interface IHasText : IDrawable
```

# クラス
## `BufferedContainerView<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/BufferedContainerView.cs#L18)
```csharp
public partial class BufferedContainerView<T> : Drawable, ITexturedShaderDrawable
    where T : Drawable
```

## `FontAwesome` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/FontAwesome.cs#L14)
```csharp
public static class FontAwesome
```

## `Sprite` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/Sprite.cs#L19)
```csharp
public partial class Sprite : Drawable, ITexturedShaderDrawable
```

## `SpriteDrawNode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/SpriteDrawNode.cs#L16)
```csharp
public class SpriteDrawNode : TexturedShaderDrawNode
```

## `SpriteIcon` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/SpriteIcon.cs#L20)
```csharp
public partial class SpriteIcon : CompositeDrawable
```

## `SpriteText` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/SpriteText.cs#L28)
```csharp
public partial class SpriteText : Drawable, IHasLineBaseHeight, ITexturedShaderDrawable, IHasText, IHasFilterTerms, IFillFlowContainer, IHasCurrentValue<string>
```

## `SpriteText` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/SpriteText_DrawNode.cs#L16)
```csharp
public partial class SpriteText
```



# 構造体
## `FontUsage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/FontUsage.cs#L14)
```csharp
public readonly struct FontUsage : IEquatable<FontUsage>
```

## `IconUsage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Sprites/IconUsage.cs#L14)
```csharp
public readonly struct IconUsage : IEquatable<IconUsage>
```