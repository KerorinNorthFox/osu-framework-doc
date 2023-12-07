# osu.Framework.Graphics.Pooling Doc
- [osu.Framework.Graphics.Pooling Doc](#osuframeworkgraphicspooling-doc)
- [インターフェース](#インターフェース)
  - [`IDrawablePool` #](#idrawablepool-)
- [クラス](#クラス)
  - [`DrawablePool<T>` #](#drawablepoolt-)
  - [`PoolableDrawable` #](#poolabledrawable-)

# インターフェース
## `IDrawablePool` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Pooling/IDrawablePool.cs#L10)
```csharp
public interface IDrawablePool
```

# クラス
## `DrawablePool<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Pooling/DrawablePool.cs#L26)
```csharp
public partial class DrawablePool<T> : CompositeDrawable, IDrawablePool where T : PoolableDrawable, new()
```

## `PoolableDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Pooling/PoolableDrawable.cs#L11)
```csharp
public partial class PoolableDrawable : CompositeDrawable
```

