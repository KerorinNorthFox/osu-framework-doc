# osu.Framework.Physics Doc
- [osu.Framework.Physics Doc](#osuframeworkphysics-doc)
- [インターフェース](#インターフェース)
  - [`IRigidBody` #](#irigidbody-)
- [クラス](#クラス)
  - [`RigidBodyExtensions` #](#rigidbodyextensions-)
  - [`RigidBodyContainer<T>` #](#rigidbodycontainert-)
  - [`RigidBodySimulation` #](#rigidbodysimulation-)
  - [`RigidBodySimulation<T>` #](#rigidbodysimulationt-)

# インターフェース
## `IRigidBody` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Physics/IRigidBody.cs#L13)
```csharp
public interface IRigidBody : IDrawable
```

# クラス
## `RigidBodyExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Physics/IRigidBody.cs#L90)
```csharp
public static class RigidBodyExtensions
```

## `RigidBodyContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Physics/RigidBodyContainer.cs#L19)
```csharp
public partial class RigidBodyContainer<T> : Container<T>, IRigidBody
    where T : Drawable
```

## `RigidBodySimulation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Physics/RigidBodySimulation.cs#L14)
```cshar
public partial class RigidBodySimulation : RigidBodySimulation<Drawable>
```

## `RigidBodySimulation<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Physics/RigidBodySimulation.cs#L21)
```csharp
public partial class RigidBodySimulation<T> : RigidBodyContainer<RigidBodyContainer<T>>
    where T : Drawable
```