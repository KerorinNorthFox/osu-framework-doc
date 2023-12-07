# osu.Framework.Graphics.Effects Doc
- [osu.Framework.Graphics.Effects Doc](#osuframeworkgraphicseffects-doc)
- [インターフェース](#インターフェース)
  - [`IEffect` #](#ieffect-)
- [クラス](#クラス)
  - [`BlurEffect` #](#blureffect-)
  - [`EdgeEffect` #](#edgeeffect-)
  - [`EffectExtensions` #](#effectextensions-)
  - [`GrowEffect` #](#groweffect-)
  - [`OutlineEffect` #](#outlineeffect-)
- [構造体](#構造体)
  - [`EdgeEffectParameters` #](#edgeeffectparameters-)
  - [列挙型](#列挙型)
  - [`EdgeEffectType` #](#edgeeffecttype-)

# インターフェース
## `IEffect` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/IEffect.cs#L10)
```csharp
public interface IEffect<out T> where T : Drawable
```

# クラス
## `BlurEffect` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/BlurEffect.cs#L15)
```csharp
public class BlurEffect : IEffect<BufferedContainer>
```

## `EdgeEffect` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/EdgeEffect.cs#L11)
```csharp
public class EdgeEffect : IEffect<Container>
```

## `EffectExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/EffectExtensions.cs#L13)
```csharp
public static class EffectExtensions
```

## `GrowEffect` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/GlowEffect.cs#L14)
```csharp
public class GlowEffect : IEffect<BufferedContainer>
```

## `OutlineEffect` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/OutlineEffect.cs#L14)
```csharp
public class OutlineEffect : IEffect<BufferedContainer>
```



# 構造体
## `EdgeEffectParameters` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/EdgeEffectParameters.cs#L14)
```csharp
public struct EdgeEffectParameters : IEquatable<EdgeEffectParameters>
```

## 列挙型
## `EdgeEffectType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Effects/EdgeEffectType.cs#L11)
```csharp
public enum EdgeEffectType
```


