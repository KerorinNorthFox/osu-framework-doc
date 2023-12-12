# osu.Framework.Utils Doc
- [osu.Framework.Utils Doc](#osuframeworkutils-doc)
- [インターフェース](#インターフェース)
  - [`IInterpolable<TValue>` #](#iinterpolabletvalue-)
- [クラス](#クラス)
  - [`Blur` #](#blur-)
  - [`General` #](#general-)
  - [`HasOrderedElementsAttribute` #](#hasorderedelementsattribute-)
  - [`IncrementalBSplineBuilder` #](#incrementalbsplinebuilder-)
  - [`Interpolation` #](#interpolation-)
  - [`MathUtils` #](#mathutils-)
  - [`NumberFormatter` #](#numberformatter-)
  - [`OrderAttribute` #](#orderattribute-)
  - [`PathApproximator` #](#pathapproximator-)
  - [`Precision` #](#precision-)
  - [`RNG` #](#rng-)
  - [`SourceGeneratorUtils` #](#sourcegeneratorutils-)
  - [`ThrowHelper` #](#throwhelper-)
  - [`Validation` #](#validation-)
- [デリゲート](#デリゲート)
  - [`InterpolationFunc<TValue, TEasing>` #](#interpolationfunctvalue-teasing-)
- [構造体](#構造体)
  - [`CircularArcProperties` #](#circulararcproperties-)
  - [`ConvexPolygonClipper<TClip, TSubject>` #](#convexpolygonclippertclip-tsubject-)

# インターフェース
## `IInterpolable<TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/IInterpolable.cs#L12)
```csharp
public interface IInterpolable<TValue>
```

# クラス
## `Blur` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/Blur.cs#L11)
```csharp
public static class Blur
```

## `General` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/General.cs#L10)
```csharp
public static class General
```

## `HasOrderedElementsAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/HasOrderedElementsAttribute.cs#L14)
```csharp
[AttributeUsage(AttributeTargets.Enum)]
public class HasOrderedElementsAttribute : Attribute
```
## `IncrementalBSplineBuilder` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/IncrementalBSplineBuilder.cs#L18)
```csharp
public class IncrementalBSplineBuilder
```

## `Interpolation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/Interpolation.cs#L16)
```csharp
public static class Interpolation
```

## `MathUtils` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/MathUtils.cs#L8)
```csharp
public static class MathUtils
```

## `NumberFormatter` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/NumberFormatter.cs#L11)
```csharp
public static class NumberFormatter
```

## `OrderAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/OrderAttribute.cs#L18)
```csharp
[AttributeUsage(AttributeTargets.Field)]
public class OrderAttribute : Attribute
```

## `PathApproximator` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/PathApproximator.cs#L16)
```csharp
public static class PathApproximator
```

## `Precision` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/Precision.cs#L13)
```csharp
public static class Precision
```

## `RNG` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/RNG.cs#L11)
```csharp
public static class RNG
```

## `SourceGeneratorUtils` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/SourceGeneratorUtils.cs#L15)
```csharp
public static class SourceGeneratorUtils
```

## `ThrowHelper` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/ThrowHelper.cs#L13)
```csharp
public static class ThrowHelper
```
## `Validation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/Validation.cs#L13)
```csharp
public static class Validation
```


# デリゲート
## `InterpolationFunc<TValue, TEasing>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/Interpolation.cs#L444)
```csharp
public delegate TValue InterpolationFunc<TValue, TEasing>(double time, TValue startValue, TValue endValue, double startTime, double endTime, in TEasing easingType) where TEasing : IEasingFunction;
```


# 構造体
## `CircularArcProperties` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/CircularArcProperties.cs#L9)
```csharp
public readonly struct CircularArcProperties
```

## `ConvexPolygonClipper<TClip, TSubject>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Utils/ConvexPolygonClipper.cs#L12)
```csharp
public readonly ref struct ConvexPolygonClipper<TClip, TSubject>
    where TClip : IConvexPolygon
    where TSubject : IConvexPolygon
```