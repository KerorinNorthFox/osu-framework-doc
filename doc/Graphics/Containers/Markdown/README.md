# osu.Framework.Graphics.Containers.Markdown Doc
- [osu.Framework.Graphics.Containers.Markdown Doc](#osuframeworkgraphicscontainersmarkdown-doc)
- [インターフェース](#インターフェース)
  - [`IMarkdownTextComponent` #](#imarkdowntextcomponent-)
  - [`IMarkdownTextFlowComponent` #](#imarkdowntextflowcomponent-)
- [クラス](#クラス)
  - [`MarkdownContainer` #](#markdowncontainer-)
  - [`MarkdownFencedCodeBlock` #](#markdownfencedcodeblock-)
  - [`MarkdownHeading` #](#markdownheading-)
  - [`MarkdownImage` #](#markdownimage-)
  - [`MarkdownLinkText` #](#markdownlinktext-)
  - [`MarkdownList` #](#markdownlist-)
  - [`MarkdownParagraph` #](#markdownparagraph-)
  - [`MarkdownQuoteBlock` #](#markdownquoteblock-)
  - [`MarkdownSeparator` #](#markdownseparator-)
  - [`MarkdownTable` #](#markdowntable-)
  - [`MarkdownTableCell` #](#markdowntablecell-)
  - [`MarkdownTextFlowContainer` #](#markdowntextflowcontainer-)
  - [`NotImplementedMarkdown` #](#notimplementedmarkdown-)

# インターフェース
## `IMarkdownTextComponent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/IMarkdownTextComponent.cs#L10)
```csharp
[Cached(typeof(IMarkdownTextComponent))]
public interface IMarkdownTextComponent
```

## `IMarkdownTextFlowComponent` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/IMarkdownTextFlowComponent.cs#L9)
```csharp
[Cached(Type = typeof(IMarkdownTextFlowComponent))]
public interface IMarkdownTextFlowComponent
```



# クラス
## `MarkdownContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownContainer.cs#L27)
```csharp
public partial class MarkdownContainer : CompositeDrawable, IMarkdownTextComponent, IMarkdownTextFlowComponent
```

## `MarkdownFencedCodeBlock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownFencedCodeBlock.cs#L19)
```csharp
public partial class MarkdownFencedCodeBlock : CompositeDrawable, IMarkdownTextFlowComponent
```

## `MarkdownHeading` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownHeading.cs#L18)
```csharp
public partial class MarkdownHeading : CompositeDrawable, IMarkdownTextFlowComponent
```

## `MarkdownImage` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownImage.cs#L18)
```csharp
public partial class MarkdownImage : CompositeDrawable
```

## `MarkdownLinkText` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownLinkText.cs#L20)
```csharp
public partial class MarkdownLinkText : CompositeDrawable, IHasTooltip, IMarkdownTextComponent
```

## `MarkdownList` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownList.cs#L15)
```csharp
public partial class MarkdownList : FillFlowContainer
```

## `MarkdownParagraph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownParagraph.cs#L12)
```csharp
public partial class MarkdownParagraph : CompositeDrawable, IMarkdownTextFlowComponent
```

## `MarkdownQuoteBlock` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownQuoteBlock.cs#L17)
```csharp
public partial class MarkdownQuoteBlock : CompositeDrawable, IMarkdownTextFlowComponent
```

## `MarkdownSeparator` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownSeparator.cs#L16)
```csharp
public partial class MarkdownSeparator : CompositeDrawable
```

## `MarkdownTable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownTable.cs#L23)
```csharp
public partial class MarkdownTable : CompositeDrawable
```

## `MarkdownTableCell` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownTableCell.cs#L20)
```csharp
public partial class MarkdownTableCell : CompositeDrawable, IMarkdownTextFlowComponent
```

## `MarkdownTextFlowContainer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/MarkdownTextFlowContainer.cs#L23)
```csharp
public partial class MarkdownTextFlowContainer : CustomizableTextContainer, IMarkdownTextComponent
```

## `NotImplementedMarkdown` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Containers/Markdown/NotImplementedMarkdown.cs#L14)
```csharp
public partial class NotImplementedMarkdown : CompositeDrawable, IMarkdownTextComponent
```

