# osu.Framework.Graphics.Transforms Doc
- [osu.Framework.Graphics.Transforms Doc](#osuframeworkgraphicstransforms-doc)
- [インターフェース](#インターフェース)
  - [`IEasingFunction` #](#ieasingfunction-)
  - [`ITransformSequence` #](#itransformsequence-)
  - [`ITransformable` #](#itransformable-)
- [クラス](#クラス)
  - [`Transform` #](#transform-)
  - [`Transform<TValue>` #](#transformtvalue-)
  - [`Transform<TValue, TEasing, T>` #](#transformtvalue-teasing-t-)
  - [`Transform<TValue, T>` #](#transformtvalue-t-)
  - [`TransformSequence<T>` #](#transformsequencet-)
  - [`Transformable` #](#transformable-)
- [構造体](#構造体)
  - [`DefaultEasingFunction` #](#defaulteasingfunction-)

# インターフェース
## `IEasingFunction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/IEasingFunction.cs#L9)
```csharp
public interface IEasingFunction
```

## `ITransformSequence` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/ITransformSequence.cs#L6)
```csharp
public interface ITransformSequence
```

## `ITransformable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/ITransformable.cs#L10)
```csharp
public interface ITransformable
```

# クラス
## `Transform` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/Transform.cs#L11)
```csharp
public abstract class Transform
```

## `Transform<TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/Transform.cs#L93)
```csharp
public abstract class Transform<TValue> : Transform
```

## `Transform<TValue, TEasing, T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/Transform.cs#L99)
```csharp
public abstract class Transform<TValue, TEasing, T> : Transform<TValue>
    where TEasing : IEasingFunction
    where T : class, ITransformable
```

## `Transform<TValue, T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/Transform.cs#L124)
```csharp
public abstract class Transform<TValue, T> : Transform<TValue, DefaultEasingFunction, T>
    where T : class, ITransformable
```

## `TransformSequence<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/TransformSequence.cs#L20)
```csharp
public class TransformSequence<T> : ITransformSequence where T : class, ITransformable
```

## `Transformable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/Transformable.cs#L20)
```csharp
public abstract partial class Transformable : ITransformable, IDependencyInjectionCandidate
```




# 構造体
## `DefaultEasingFunction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Transforms/DefaultEasingFunction.cs#L11)
```csharp
public readonly struct DefaultEasingFunction : IEasingFunction
```