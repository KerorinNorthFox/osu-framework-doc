# osu.Framework.IO.Stores Doc
- [osu.Framework.IO.Stores Doc](#osuframeworkiostores-doc)
- [インターフェース](#インターフェース)
  - [`IGlyphStore` #](#iglyphstore-)
  - [`IResourceStore` #](#iresourcestore-)
- [クラス](#クラス)
  - [`DllResourceStore` #](#dllresourcestore-)
  - [`FontStore` #](#fontstore-)
  - [`GlyphStore` #](#glyphstore-)
  - [`ResourceStoreExtensions` #](#resourcestoreextensions-)
  - [`NamespacedResourceStore<T>` #](#namespacedresourcestoret-)
  - [`OnlineStore` #](#onlinestore-)
  - [`RawCachingGlyphStore` #](#rawcachingglyphstore-)
  - [`ResourceStore<T>` #](#resourcestoret-)
  - [`StorageBackedResourceStore` #](#storagebackedresourcestore-)
  - [`TimedExpiryGlyphStore` #](#timedexpiryglyphstore-)

# インターフェース
## `IGlyphStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/IGlyphStore.cs#L12)
```csharp
public interface IGlyphStore : IResourceStore<CharacterGlyph>
```

## `IResourceStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/IResourceStore.cs#L19)
```csharp
public interface IResourceStore<T> : IDisposable
    where T : class
```


# クラス
## `DllResourceStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/DllResourceStore.cs#L18)
```csharp
public class DllResourceStore : IResourceStore<byte[]>
```

## `FontStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/FontStore.cs#L18)
```csharp
public class FontStore : TextureStore, ITexturedGlyphLookupStore
```

## `GlyphStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/GlyphStore.cs#L29)
```csharp
public class GlyphStore : IResourceStore<TextureUpload>, IGlyphStore
```

## `ResourceStoreExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/IResourceStore.cs#L46)
```csharp
public static class ResourceStoreExtensions
```

## `NamespacedResourceStore<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/NamespacedResourceStore.cs#L10)
```csharp
public class NamespacedResourceStore<T> : ResourceStore<T>
    where T : class
```

## `OnlineStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/OnlineStore.cs#L16)
```csharp
public class OnlineStore : IResourceStore<byte[]>
```

## `RawCachingGlyphStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/RawCachingGlyphStore.cs#L29)
```csharp
public class RawCachingGlyphStore : GlyphStore
```

## `ResourceStore<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/ResourceStore.cs#L15)
```csharp
public class ResourceStore<T> : IResourceStore<T>
    where T : class
```

## `StorageBackedResourceStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/StorageBackedResourceStore.cs#L19)
```csharp
public class StorageBackedResourceStore : IResourceStore<byte[]>
```

## `TimedExpiryGlyphStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IO/Stores/TimedExpiryGlyphStore.cs#L20)
```csharp
public class TimedExpiryGlyphStore : GlyphStore
```