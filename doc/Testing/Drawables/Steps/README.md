# osu.Framework.Testing.Drawables.Steps Doc
- [osu.Framework.Testing.Drawables.Steps Doc](#osuframeworktestingdrawablessteps-doc)
- [クラス](#クラス)
  - [`AssertButton` #](#assertbutton-)
  - [`LabelStep` #](#labelstep-)
  - [`RepeatStepButton` #](#repeatstepbutton-)
  - [`SingleStepButton` #](#singlestepbutton-)
  - [`StepButton` #](#stepbutton-)
  - [`StepSlider<T>` #](#stepslidert-)
  - [`ToggleStepButton` #](#togglestepbutton-)
  - [`UntilStepButton` #](#untilstepbutton-)

# クラス
## `AssertButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/AssertButton.cs#L13)
```csharp
public partial class AssertButton : StepButton
```

## `LabelStep` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/LabelStep.cs#L8)
```csharp
public partial class LabelStep : StepButton
```

## `RepeatStepButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/RepeatStepButton.cs#L10)
```csharp
public partial class RepeatStepButton : StepButton
```

## `SingleStepButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/SingleStepButton.cs#L10)
```csharp
public partial class SingleStepButton : StepButton
```

## `StepButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/StepButton.cs#L17)
```csharp
public abstract partial class StepButton : CompositeDrawable
```

## `StepSlider<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/StepSlider.cs#L19)
```csharp
public partial class StepSlider<T> : SliderBar<T>
    where T : struct, IComparable<T>, IConvertible, IEquatable<T>
```

## `ToggleStepButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/ToggleStepButton.cs#L10)
```csharp
public partial class ToggleStepButton : StepButton
```

## `UntilStepButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/Drawables/Steps/UntilStepButton.cs#L14)
```csharp
public partial class UntilStepButton : StepButton
```