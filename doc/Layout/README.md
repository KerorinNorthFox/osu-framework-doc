# osu.Framework.Layout Doc
- [osu.Framework.Layout Doc](#osuframeworklayout-doc)
- [クラス](#クラス)
  - [`LayoutMember` #](#layoutmember-)
  - [`LayoutValue` #](#layoutvalue-)
  - [`LayoutValue<T>` #](#layoutvaluet-)
- [デリゲート](#デリゲート)
  - [`InvalidationConditionDelegate` #](#invalidationconditiondelegate-)
- [列挙型](#列挙型)
  - [`InvalidationSource` #](#invalidationsource-)

# クラス
## `LayoutMember` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Layout/LayoutMember.cs#L13)
```csharp
public abstract class LayoutMember
```

## `LayoutValue` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Layout/LayoutValue.cs#L15)
```csharp
public class LayoutValue : LayoutMember
```

## `LayoutValue<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Layout/LayoutValue.cs#L39)
```csharp
public class LayoutValue<T> : LayoutMember
```

# デリゲート
## `InvalidationConditionDelegate` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Layout/LayoutMember.cs#L92)
```csharp
public delegate bool InvalidationConditionDelegate(Drawable source, Invalidation invalidation);
```

# 列挙型
## `InvalidationSource` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Layout/InvalidationSource.cs#L13)
```csharp
public enum InvalidationSource
```