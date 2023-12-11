# osu.Framework.Localisation Doc
- [osu.Framework.Localisation Doc](#osuframeworklocalisation-doc)
- [インターフェース](#インターフェース)
  - [`ILocaliasbleStringData` #](#ilocaliasblestringdata-)
  - [`ILocalisationStore` #](#ilocalisationstore-)
  - [`ILocalisedBindableString` #](#ilocalisedbindablestring-)
- [クラス](#クラス)
  - [`CaseTransformableString` #](#casetransformablestring-)
  - [`CultureInfoHelper` #](#cultureinfohelper-)
  - [`LocaleMapping` #](#localemapping-)
  - [`LocalisableDescriptionAttribute` #](#localisabledescriptionattribute-)
  - [`LocalisableFormattableString` #](#localisableformattablestring-)
  - [`LocalisableStringEqualityComparer` #](#localisablestringequalitycomparer-)
  - [`LocalisationManager` #](#localisationmanager-)
  - [`LocalisationManager` #](#localisationmanager--1)
  - [`LocalisationParameters` #](#localisationparameters-)
  - [`RomanisableString` #](#romanisablestring-)
  - [`TranslatableString` #](#translatablestring-)
- [構造体](#構造体)
  - [`LocalisableString` #](#localisablestring-)
- [列挙型](#列挙型)
  - [`Casing` #](#casing-)

# インターフェース
## `ILocaliasbleStringData` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/ILocalisableStringData.cs#L11)
```csharp
public interface ILocalisableStringData : IEquatable<ILocalisableStringData>
```

## `ILocalisationStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/ILocalisationStore.cs#L11)
```csharp
public interface ILocalisationStore : IResourceStore<string>
```

## `ILocalisedBindableString` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/ILocalisedBindableString.cs#L11)
```csharp
public interface ILocalisedBindableString : IBindable<string>
```


# クラス
## `CaseTransformableString` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/CaseTransformableString.cs#L12)
```csharp
namespace osu.Framework.Localisation
```

## `CultureInfoHelper` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/CultureInfoHelper.cs#L11)
```csharp
public static class CultureInfoHelper
```

## `LocaleMapping` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocaleMapping.cs#L10)
```csharp
public class LocaleMapping
```

## `LocalisableDescriptionAttribute` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisableDescriptionAttribute.cs#L36)
```csharp
[AttributeUsage(AttributeTargets.All)]
    public sealed class LocalisableDescriptionAttribute : Attribute
```

## `LocalisableFormattableString` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisableFormattableString.cs#L14)
```csharp
public class LocalisableFormattableString : IEquatable<LocalisableFormattableString>, ILocalisableStringData
```

## `LocalisableStringEqualityComparer` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisableStringEqualityComparer.cs#L14)
```csharp
public class LocalisableStringEqualityComparer : IEqualityComparer<LocalisableString>
```

## `LocalisationManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisationManager.cs#L15)
```csharp
public partial class LocalisationManager : IDisposable
```

## `LocalisationManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisationManager_LocalisedBindableString.cs#L12)
```csharp
public partial class LocalisationManager
```

## `LocalisationParameters` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisationParameters.cs#L9)
```csharp
public class LocalisationParameters
```

## `RomanisableString` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/RomanisableString.cs#L13)
```csharp
public class RomanisableString : IEquatable<RomanisableString>, ILocalisableStringData
```

## `TranslatableString` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/TranslatableString.cs#L11)
```csharp
public class TranslatableString : LocalisableFormattableString, IEquatable<TranslatableString>
```



# 構造体
## `LocalisableString` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/LocalisableString.cs#L13)
```csharp
public readonly struct LocalisableString : IEquatable<LocalisableString>
```



# 列挙型
## `Casing` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Localisation/CaseTransformableString.cs#L102)
```csharp

```public enum Casing