# osu.Framework.Testing Doc
- [osu.Framework.Testing Doc](#osuframeworktesting-doc)
- [インターフェース](#インターフェース)
  - [`ITestSceneTestRunner` #](#itestscenetestrunner-)
- [クラス](#クラス)
  - [`GridtTestScene` #](#gridttestscene-)
  - [`HeadlessTestAttribute` #](#headlesstestattribute-)
  - [`ManualInputManagerTestScene` #](#manualinputmanagertestscene-)
  - [`MenuTestScene` #](#menutestscene-)
  - [`SetupStepsAttribute` #](#setupstepsattribute-)
  - [`TearDownStepsAttribute` #](#teardownstepsattribute-)
  - [`TemporaryNativeStorage` #](#temporarynativestorage-)
  - [`TestBrowser` #](#testbrowser-)
  - [`TestBrowserTestRunner` #](#testbrowsertestrunner-)
  - [`TestRunHeadlessGameHost` #](#testrunheadlessgamehost-)
  - [`TestScene` #](#testscene-)
  - [`TestSceneTestRunner` #](#testscenetestrunner-)
  - [`TestingExtensions` #](#testingextensions-)
- [列挙型](#列挙型)
  - [`TestBrowserAction` #](#testbrowseraction-)

# インターフェース
## `ITestSceneTestRunner` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestSceneTestRunner.cs#L94)
```csharp
public interface ITestSceneTestRunner
```

# クラス
## `GridtTestScene` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/GridTestScene.cs#L14)
```csharp
public abstract partial class GridTestScene : TestScene
```

## `HeadlessTestAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/HeadlessTestAttribute.cs#L15)
```csharp
[AttributeUsage(AttributeTargets.Class)]
    [MeansImplicitUse]
    public class HeadlessTestAttribute : Attribute
```

## `ManualInputManagerTestScene` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/ManualInputManagerTestScene.cs#L21)
```csharp
public abstract partial class ManualInputManagerTestScene : TestScene
```

## `MenuTestScene` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/MenuTestScene.cs#L19)
```csharp
public abstract partial class MenuTestScene : ManualInputManagerTestScene
```

## `SetupStepsAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/SetUpStepsAttribute.cs#L15)
```csharp
[AttributeUsage(AttributeTargets.Method)]
[MeansImplicitUse]
public class SetUpStepsAttribute : Attribute
```

## `TearDownStepsAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TearDownStepsAttribute.cs#L15)
```csharp
[AttributeUsage(AttributeTargets.Method)]
[MeansImplicitUse]
public class TearDownStepsAttribute : Attribute
```

## `TemporaryNativeStorage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TemporaryNativeStorage.cs#L16)
```csharp
public class TemporaryNativeStorage : NativeStorage, IDisposable
```

## `TestBrowser` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestBrowser.cs#L42)
```csharp
[Cached]
public partial class TestBrowser : KeyBindingContainer<TestBrowserAction>, IKeyBindingHandler<TestBrowserAction>, IHandleGlobalKeyboardInput
```

## `TestBrowserTestRunner` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestBrowserTestRunner.cs#L17)
```csharp
public partial class TestBrowserTestRunner : CompositeDrawable
```

## `TestRunHeadlessGameHost` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestRunHeadlessGameHost.cs#L18)
```csharp
public class TestRunHeadlessGameHost : HeadlessGameHost
```

## `TestScene` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestScene.cs#L35)
```csharp
[TestFixture]
public abstract partial class TestScene : Container
```

## `TestSceneTestRunner` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestSceneTestRunner.cs#L19)
```csharp
public partial class TestSceneTestRunner : Game, ITestSceneTestRunner
```

## `TestingExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestingExtensions.cs#L10)
```csharp
public static class TestingExtensions
```



# 列挙型
## `TestBrowserAction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Testing/TestBrowser.cs#L681)
```csharp
public enum TestBrowserAction
```