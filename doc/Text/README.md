# osu.Framework.Text Doc
- [osu.Framework.Text Doc](#osuframeworktext-doc)
- [インターフェース](#インターフェース)
  - [`ICharacterGlyph` #](#icharacterglyph-)
  - [`ITexturedCharacterGlyph` #](#itexturedcharacterglyph-)
  - [`ITexturedGlyphLookupStore` #](#itexturedglyphlookupstore-)
- [クラス](#クラス)
  - [`CharacterGlyph` #](#characterglyph-)
  - [`TexturedCharacterGlyphExtensions` #](#texturedcharacterglyphextensions-)
  - [`MultilineTextBuilder` #](#multilinetextbuilder-)
  - [`TextBuilder` #](#textbuilder-)
  - [`TexturedCharacterGlyph` #](#texturedcharacterglyph-)
  - [`TruncatingTextBuilder` #](#truncatingtextbuilder-)
- [構造体](#構造体)
  - [`TextBuilderGlyph` #](#textbuilderglyph-)

# インターフェース
## `ICharacterGlyph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/ICharacterGlyph.cs#L9)
```csharp
public interface ICharacterGlyph
```

## `ITexturedCharacterGlyph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/ITexturedCharacterGlyph.cs#L11)
```csharp
public interface ITexturedCharacterGlyph : ICharacterGlyph
```

## `ITexturedGlyphLookupStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/ITexturedGlyphLookupStore.cs#L8)
```csharp
public interface ITexturedGlyphLookupStore
```

# クラス
## `CharacterGlyph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/CharacterGlyph.cs#L12)
```csharp
public sealed class CharacterGlyph : ICharacterGlyph
```

## `TexturedCharacterGlyphExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/ITexturedCharacterGlyph.cs#L29)
```csharp
public static class TexturedCharacterGlyphExtensions
```

## `MultilineTextBuilder` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/MultilineTextBuilder.cs#L12)
```csharp
public sealed class MultilineTextBuilder : TextBuilder
```

## `TextBuilder` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/TextBuilder.cs#L18)
```csharp
public class TextBuilder : IHasLineBaseHeight
```

## `TexturedCharacterGlyph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/TexturedCharacterGlyph.cs#L9)
```csharp
public sealed class TexturedCharacterGlyph : ITexturedCharacterGlyph
```

## `TruncatingTextBuilder` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/TruncatingTextBuilder.cs#L12)
```csharp
public sealed class TruncatingTextBuilder : TextBuilder
```

# 構造体
## `TextBuilderGlyph` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Text/TextBuilderGlyph.cs#L13)
```csharp

```