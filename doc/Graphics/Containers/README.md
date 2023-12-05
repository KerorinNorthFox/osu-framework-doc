# osu.Framework.Graphics.Containers Doc
- [osu.Framework.Graphics.Containers Doc](#osuframeworkgraphicscontainers-doc)
- [インターフェース](#インターフェース)
  - [`IBufferedContainer` #](#ibufferedcontainer-)
  - [`IConditionalFilterable` #](#iconditionalfilterable-)
  - [`IContainer` #](#icontainer-)
  - [`IContainerEnumerable<out T>` #](#icontainerenumerableout-t-)
  - [`IContainerCollection<in T>` #](#icontainercollectionin-t-)
  - [`IFillFlowContainer` #](#ifillflowcontainer-)
  - [`IFilterable` #](#ifilterable-)
  - [`IHasFilterTerms` #](#ihasfilterterms-)
  - [`IHasFilterableChildren` #](#ihasfilterablechildren-)
  - [`ISafeArea` #](#isafearea-)
  - [`IScrollContainer` #](#iscrollcontainer-)
  - [`ITextPart` #](#itextpart-)
  - [`ITabbableContainer` #](#itabbablecontainer-)
- [クラス](#クラス)
  - [`AudioContainer<T>` #](#audiocontainert-)
  - [`AudioContainer` #](#audiocontainer-)
  - [`BasicScrollContainer` #](#basicscrollcontainer-)
  - [`BasicScrollContainer<T>` #](#basicscrollcontainert-)
  - [`BufferedContainer` #](#bufferedcontainer-)
  - [`BufferedContainer<T>` #](#bufferedcontainert-)
  - [`BufferedContainer<T>` #](#bufferedcontainert--1)
  - [`CircularContainer` #](#circularcontainer-)
  - [`ClickableContainer` #](#clickablecontainer-)
  - [`CompositeComponent` #](#compositecomponent-)
  - [`CompositeDrawable` #](#compositedrawable-)
  - [`CompositeDrawable` #](#compositedrawable--1)
  - [`Container` #](#container-)
  - [`Container<T>` #](#containert-)
  - [`ContainerExtensions` #](#containerextensions-)
  - [`CustomizableTextContainer` #](#customizabletextcontainer-)
  - [`DelayedLoadUnloadWrapper` #](#delayedloadunloadwrapper-)
  - [`DelayedLoadWrapper` #](#delayedloadwrapper-)
  - [`DrawSizePreservingFillContainer` #](#drawsizepreservingfillcontainer-)
  - [`FillFlowContainer` #](#fillflowcontainer-)
  - [`FillFlowContainer<T>` #](#fillflowcontainert-)
  - [`FlowContainer<T>` #](#flowcontainert-)
  - [`FocusedOverlayContainer` #](#focusedoverlaycontainer-)
  - [`GridContainer` #](#gridcontainer-)
  - [`Dimension` #](#dimension-)
  - [`GridContainerContent` #](#gridcontainercontent-)
  - [`LifetimeManagementContainer` #](#lifetimemanagementcontainer-)
  - [`ModelBackedDrawable<T>` #](#modelbackeddrawablet-)
  - [`OverlayContainer` #](#overlaycontainer-)
  - [`RearrangeableListContainer<TModel>` #](#rearrangeablelistcontainertmodel-)
  - [`RearrangeableListItem<TModel>` #](#rearrangeablelistitemtmodel-)
  - [`SafeAreaContainer` #](#safeareacontainer-)
  - [`SafeAreaDefinintContainer` #](#safeareadefinintcontainer-)
  - [`ScrollContainer<T>` #](#scrollcontainert-)
  - [`SearchContainer` #](#searchcontainer-)
  - [`SearchContainer<T>` #](#searchcontainert-)
  - [`TabbableContainer` #](#tabbablecontainer-)
  - [`TabbableContainer<T>` #](#tabbablecontainert-)
  - [`TableContainer` #](#tablecontainer-)
  - [`TableColumn` #](#tablecolumn-)
  - [`TextChunk` #](#textchunk-)
  - [`TextFlowContainer` #](#textflowcontainer-)
  - [`TextNewLine` #](#textnewline-)
  - [`TextPart` #](#textpart-)
  - [`TextPartManual` #](#textpartmanual-)
  - [`VisibilityContainer` #](#visibilitycontainer-)
- [構造体](#構造体)
  - [`LifetimeBoundaryCrossedEvent` #](#lifetimeboundarycrossedevent-)
- [列挙型](#列挙型)
  - [`EffectPlacement` #](#effectplacement-)
  - [`DrawSizePreservationStrategy` #](#drawsizepreservationstrategy-)
  - [`FillDirection` #](#filldirection-)
  - [`GridSizeMode` #](#gridsizemode-)
  - [`Visibility` #](#visibility-)

# インターフェース
## `IBufferedContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IBufferedContainer.cs#L8)
```csharp
public interface IBufferedContainer : IContainer
```

## `IConditionalFilterable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IConditionalFilterable.cs#L15)
```csharp
public interface IConditionalFilterable : IFilterable
```

## `IContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IContainer.cs#L11)
```csharp
public interface IContainer : IDrawable
```

## `IContainerEnumerable<out T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IContainer.cs#L20)
```csharp
public interface IContainerEnumerable<out T> : IContainer
    where T : class, IDrawable
```

## `IContainerCollection<in T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IContainer.cs#L38)
```csharp
public interface IContainerCollection<in T> : IContainer
    where T : class, IDrawable
```

## `IFillFlowContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IFillFlowContainer.cs#L9)
```csharp
public interface IFillFlowContainer : ITransformable
```

## `IFilterable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IFilterable.cs#L10)
```csharp
public interface IFilterable : IHasFilterTerms
```

## `IHasFilterTerms` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IHasFilterTerms.cs#L13)
```csharp
public interface IHasFilterTerms
```

## `IHasFilterableChildren` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IHasFilterableChildren.cs#L10)
```csharp
[Obsolete("IFilterable children are now looked up automatically. Implementors of this interface should implement IFilterable directly instead.")] // can be removed 20230512
public interface IHasFilterableChildren : IFilterable
```

## `ISafeArea` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/ISafeArea.cs#L12)
```csharp
public interface ISafeArea : IContainer
```

## `IScrollContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/IScrollContainer.cs#L6)
```csharp
public interface IScrollContainer : IContainer
```

## `ITextPart` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/ITextPart.cs#L14)
```csharp
public interface ITextPart
```

## `ITabbableContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TabbableContainer.cs#L20)
```csharp
public interface ITabbableContainer
```



# クラス
## `AudioContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/AudioContainer.cs#L22)
```csharp
public partial class AudioContainer<T> : DrawableAudioWrapper, IContainerEnumerable<T>, IContainerCollection<T>, ICollection<T>, IReadOnlyList<T>
    where T : Drawable
```

## `AudioContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/AudioContainer.cs#L161)
```csharp
public partial class AudioContainer : AudioContainer<Drawable>
```

## `BasicScrollContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/BasicScrollContainer.cs#L9)
```csharp
public partial class BasicScrollContainer : BasicScrollContainer<Drawable>
```

## `BasicScrollContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/BasicScrollContainer.cs#L17)
```csharp
public partial class BasicScrollContainer<T> : ScrollContainer<T>
    where T : Drawable
```

## `BufferedContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/BufferedContainer.cs#L28)
```csharp
public partial class BufferedContainer : BufferedContainer<Drawable>
```

## `BufferedContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/BufferedContainer.cs#L44)
```csharp
public partial class BufferedContainer<T> : Container<T>, IBufferedContainer, IBufferedDrawable
    where T : Drawable
```

## `BufferedContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/BufferedContainer_DrawNode.cs#L20)
```csharp
public partial class BufferedContainer<T>
```

## `CircularContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/CircularContainer.cs#L11)
```csharp
public partial class CircularContainer : Container
```

## `ClickableContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/ClickableContainer.cs#L12)
```csharp
public partial class ClickableContainer : Container
```

## `CompositeComponent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/CompositeComponent.cs#L11)
```csharp
public abstract partial class CompositeComponent : CompositeDrawable
```

## `CompositeDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/CompositeDrawable.cs#L43)
```csharp
public abstract partial class CompositeDrawable : Drawable
```

## `CompositeDrawable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/CompositeDrawable_DrawNode.cs#L18)
```csharp
public partial class CompositeDrawable
```

## `Container` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Container.cs#L26)
```csharp
public partial class Container : Container<Drawable>
```

## `Container<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Container.cs#L36)
```csharp
public partial class Container<T> : CompositeDrawable, IContainerEnumerable<T>, IContainerCollection<T>, ICollection<T>, IReadOnlyList<T>
    where T : Drawable
```

## `ContainerExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/ContainerExtensions.cs#L14)
```csharp
public static class ContainerExtensions
```

## `CustomizableTextContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/CustomizableTextContainer.cs#L15)
```csharp
public partial class CustomizableTextContainer : TextFlowContainer
```

## `DelayedLoadUnloadWrapper` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/DelayedLoadUnloadWrapper.cs#L15)
```csharp
public partial class DelayedLoadUnloadWrapper : DelayedLoadWrapper
```

## `DelayedLoadWrapper` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/DelayedLoadWrapper.cs#L21)
```csharp
public partial class DelayedLoadWrapper : CompositeDrawable
```

## `DrawSizePreservingFillContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/DrawSizePreservingFillContainer.cs#L15)
```csharp
public partial class DrawSizePreservingFillContainer : Container
```

## `FillFlowContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/FillFlowContainer.cs#L28)
```csharp
public partial class FillFlowContainer : FillFlowContainer<Drawable>
```

## `FillFlowContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/FillFlowContainer.cs#L44)
```csharp
public partial class FillFlowContainer<T> : FlowContainer<T>, IFillFlowContainer where T : Drawable
```

## `FlowContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/FlowContainer.cs#L19)
```csharp
public abstract partial class FlowContainer<T> : Container<T>
    where T : Drawable
```

## `FocusedOverlayContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/FocusedOverlayContainer.cs#L11)
```csharp
public abstract partial class FocusedOverlayContainer : OverlayContainer
```

## `GridContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/GridContainer.cs#L21)
```csharp
public partial class GridContainer : CompositeDrawable
```

## `Dimension` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/GridContainer.cs#L381)
```csharp
public class Dimension
```

## `GridContainerContent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/GridContainerContent.cs#L14)
```csharp
public class GridContainerContent : ObservableArray<ObservableArray<Drawable>>
```

## `LifetimeManagementContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/LifetimeManagementContainer.cs#L22)
```csharp
public partial class LifetimeManagementContainer : CompositeDrawable
```

## `ModelBackedDrawable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/ModelBackedDrawable.cs#L15)
```csharp
public abstract partial class ModelBackedDrawable<T> : CompositeDrawable
```

## `OverlayContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/OverlayContainer.cs#L13)
```csharp
public abstract partial class OverlayContainer : VisibilityContainer
```

## `RearrangeableListContainer<TModel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/RearrangeableListContainer.cs#L24)
```csharp
public abstract partial class RearrangeableListContainer<TModel> : CompositeDrawable
```

## `RearrangeableListItem<TModel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/RearrangeableListItem.cs#L16)
```csharp
public abstract partial class RearrangeableListItem<TModel> : CompositeDrawable
```

## `SafeAreaContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/SafeAreaContainer.cs#L20)
```csharp
public partial class SafeAreaContainer : Container
```

## `SafeAreaDefinintContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/SafeAreaDefiningContainer.cs#L20)
```csharp
[Cached(typeof(ISafeArea))]
public partial class SafeAreaDefiningContainer : Container<Drawable>, ISafeArea
```

## `ScrollContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/ScrollContainer.cs#L19)
```csharp
public abstract partial class ScrollContainer<T> : Container<T>, IScrollContainer, DelayedLoadWrapper.IOnScreenOptimisingContainer, IKeyBindingHandler<PlatformAction>
    where T : Drawable
```

## `SearchContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/SearchContainer.cs#L17)
```csharp
public partial class SearchContainer : SearchContainer<Drawable>
```

## `SearchContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/SearchContainer.cs#L34)
```csharp
public partial class SearchContainer<T> : FillFlowContainer<T> where T : Drawable
```

## `TabbableContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TabbableContainer.cs#L13)
```csharp
public partial class TabbableContainer : TabbableContainer<Drawable>
```

## `TabbableContainer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TabbableContainer.cs#L28)
```csharp
public partial class TabbableContainer<T> : Container<T>, ITabbableContainer
    where T : Drawable
```

## `TableContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TableContainer.cs#L18)
```csharp
public partial class TableContainer : CompositeDrawable
```

## `TableColumn` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TableContainer.cs#L264)
```csharp
public class TableColumn
```

## `TextChunk` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TextChunk.cs#L16)
```csharp
public class TextChunk<TSpriteText> : TextPart
    where TSpriteText : SpriteText, new()
```

## `TextFlowContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TextFlowContainer.cs#L22)
```csharp
public partial class TextFlowContainer : FillFlowContainer
```

## `TextNewLine` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TextNewLine.cs#L9)
```csharp
public class TextNewLine : TextPart
```

## `TextPart` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TextPart.cs#L16)
```csharp
public abstract class TextPart : ITextPart
```

## `TextPartManual` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/TextPartManual.cs#L14)
```csharp
public class TextPartManual : ITextPart
```

## `VisibilityContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/VisibilityContainer.cs#L11)
```csharp
public abstract partial class VisibilityContainer : Container
```




# 構造体
## `LifetimeBoundaryCrossedEvent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/LifetimeManagementContainer.cs#L149)
```csharp
public readonly struct LifetimeBoundaryCrossedEvent
```




# 列挙型
## `EffectPlacement` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/BufferedContainer.cs#L178)
```csharp
public enum EffectPlacement
```

## `DrawSizePreservationStrategy` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/DrawSizePreservingFillContainer.cs#L78)
```csharp
public enum DrawSizePreservationStrategy
```

## `FillDirection` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/FillFlowContainer.cs#L308)
```csharp
public enum FillDirection
```

## `GridSizeMode` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/GridContainer.cs#L431)
```csharp
public enum GridSizeMode
```

## `Visibility` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/VisibilityContainer.cs#L96)
```csharp
public enum Visibility
```
