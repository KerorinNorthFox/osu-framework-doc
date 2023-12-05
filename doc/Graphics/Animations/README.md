# osu.Framework.Graphics.Animations Doc
- [osu.Framework.Graphics.Animations Doc](#osuframeworkgraphicsanimations-doc)
- [インターフェース](#インターフェース)
  - [`IAnimation` #](#ianimation-)
  - [`IFramedAnimation` #](#iframedanimation-)
- [クラス](#クラス)
  - [`Animation<T>` #](#animationt-)
  - [`AnimationClockComposite` #](#animationclockcomposite-)
  - [`CustomisableSizeCompositeDrawable` #](#customisablesizecompositedrawable-)
  - [`DrawableAnimation` #](#drawableanimation-)
  - [`FramedAnimationExtensions` #](#framedanimationextensions-)
  - [`TextureAnimation` #](#textureanimation-)
- [構造体](#構造体)
  - [`FrameData<T>` #](#framedatat-)


# インターフェース
## `IAnimation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/IAnimation.cs#L4)
```csharp
public interface IAnimation
```

## `IFramedAnimation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/IFramedAnimation.cs#L9)
```csharp
public interface IFramedAnimation : IAnimation
```




# クラス
## `Animation<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/Animation.cs#L15)
```csharp
public abstract partial class Animation<T> : AnimationClockComposite, IFramedAnimation
```

## `AnimationClockComposite` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/AnimationClockComposite.cs#L11)
```csharp
public abstract partial class AnimationClockComposite : CustomisableSizeCompositeDrawable, IAnimation
```

## `CustomisableSizeCompositeDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/CustomisableSizeCompositeDrawable.cs#L12)
```csharp
public abstract partial class CustomisableSizeCompositeDrawable : CompositeDrawable
```

## `DrawableAnimation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/DrawableAnimation.cs#L15)
```csharp
public partial class DrawableAnimation : Animation<Drawable>
```

## `FramedAnimationExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/FramedAnimationExtensions.cs#L9)
```csharp
public static class FramedAnimationExtensions
```

## `TextureAnimation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/TextureAnimation.cs#L15)
```csharp
public partial class TextureAnimation : Animation<Texture>
```



# 構造体
## `FrameData<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Animations/FrameData.cs#L10)
```csharp
public struct FrameData<T>
```
