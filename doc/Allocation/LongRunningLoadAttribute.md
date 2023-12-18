- [Class LongRunningLoadAttribute #](#class-longrunningloadattribute-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)



# Class LongRunningLoadAttribute [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/LongRunningLoadAttribute.cs#L17)
[BackgroundDependencyLoaderAttribute]()メソッドで CPU を集中的に使用しない長時間実行タスクを実行するコンポーネントを示す。<br>
長時間実行されるタスクは、優先度の低いスレッド プールにスケジュールされる。<br>
これにより、直接のコンシューマはコンポーネントをロードするときに[CompositeDrawable.LoadComponentAsync\<TLoadable\>]()を使用するようになる。


## Namespace
osu.Framework.Allocation


## Implements
[Attribute]()


## Syntax
```csharp
[AttributeUsage(AttributeTargets.Class)]
public class LongRunningLoadAttribute : Attribute
```