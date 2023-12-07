# osu.Framework.Graphics.Cursor Doc
- [osu.Framework.Graphics.Cursor Doc](#osuframeworkgraphicscursor-doc)
- [インターフェース](#インターフェース)
  - [`IHasAppearDelay` #](#ihasappeardelay-)
  - [`IHasContextMenu` #](#ihascontextmenu-)
  - [`IHasCustomTooltip` #](#ihascustomtooltip-)
  - [`IHasCustomTooltip<TContext>` #](#ihascustomtooltiptcontext-)
  - [`IHasPopover` #](#ihaspopover-)
  - [`IHasTooltip` #](#ihastooltip-)
  - [`ITooltip` #](#itooltip-)
  - [`ITooltip<in T>` #](#itooltipin-t-)
  - [`ITooltipContentProvider` #](#itooltipcontentprovider-)
- [クラス](#クラス)
  - [`BasicContextMenuContainer` #](#basiccontextmenucontainer-)
  - [`ContextMenuContainer` #](#contextmenucontainer-)
  - [`CursorContainer` #](#cursorcontainer-)
  - [`CursorEffectContainer` #](#cursoreffectcontainer-)
  - [`PopoverContainer` #](#popovercontainer-)
  - [`TooltipContainer` #](#tooltipcontainer-)
  - [`TouchLongPressFeedback` #](#touchlongpressfeedback-)

# インターフェース
## `IHasAppearDelay` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/IHasAppearDelay.cs#L9)
```csharp
public interface IHasAppearDelay : ITooltipContentProvider
```

## `IHasContextMenu` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/IHasContextMenu.cs#L8)
```csharp
public interface IHasContextMenu : IDrawable
```

## `IHasCustomTooltip` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/IHasCustomTooltip.cs#L10)
```csharp
public interface IHasCustomTooltip : ITooltipContentProvider
```

## `IHasCustomTooltip<TContext>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/IHasCustomTooltip.cs#L29)
```csharp
public interface IHasCustomTooltip<TContent> : IHasCustomTooltip
```

## `IHasPopover` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/IHasPopover.cs#L11)
```csharp
public interface IHasPopover : IDrawable
```

## `IHasTooltip` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/IHasTooltip.cs#L12)
```csharp
public interface IHasTooltip : ITooltipContentProvider
```

## `ITooltip` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/ITooltip.cs#L11)
```csharp
public interface ITooltip : IDrawable
```

## `ITooltip<in T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/ITooltip.cs#L27)
```csharp
public interface ITooltip<in T> : ITooltip
```

## `ITooltipContentProvider` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/ITooltipContentProvider.cs#L9)
```csharp
public interface ITooltipContentProvider : IDrawable
```



# クラス
## `BasicContextMenuContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/BasicContextMenuContainer.cs#L8)
```csharp
public partial class BasicContextMenuContainer : ContextMenuContainer
```
## `ContextMenuContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/ContextMenuContainer.cs#L23)
```csharp
public abstract partial class ContextMenuContainer : CursorEffectContainer<ContextMenuContainer, IHasContextMenu>
```

## `CursorContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/CursorContainer.cs#L17)
```csharp
public partial class CursorContainer : VisibilityContainer, IRequireHighFrequencyMousePosition
```

## `CursorEffectContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/CursorEffectContainer.cs#L14)
```csharp
public abstract partial class CursorEffectContainer<TSelf, TTarget> : Container
    where TSelf : CursorEffectContainer<TSelf, TTarget>
    where TTarget : class, IDrawable
```

## `PopoverContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/PopoverContainer.cs#L16)
```csharp
public partial class PopoverContainer : Container
```

## `TooltipContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/TooltipContainer.cs#L23)
```csharp
public partial class TooltipContainer : CursorEffectContainer<TooltipContainer, ITooltipContentProvider>
```

## `TouchLongPressFeedback` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Cursor/TouchLongPressFeedback.cs#L8)
```csharp
public abstract partial class TouchLongPressFeedback : CompositeDrawable
```
