# osu.Framework.Lists Doc
- [osu.Framework.Lists Doc](#osuframeworklists-doc)
- [インターフェース](#インターフェース)
  - [`INotifyArrayChanged` #](#inotifyarraychanged-)
  - [`IWeakList<T>` #](#iweaklistt-)
- [クラス](#クラス)
  - [`FuncEqualityComparer<T>` #](#funcequalitycomparert-)
  - [`LazyList<TSource, TTarget>` #](#lazylisttsource-ttarget-)
  - [`LockedWeakList<T>` #](#lockedweaklistt-)
  - [`ObservableArray<T>` #](#observablearrayt-)
  - [`SortedList<T>` #](#sortedlistt-)
  - [`WeakList<T>` #](#weaklistt-)
  - [`WeakList<T>` #](#weaklistt--1)
- [構造体](#構造体)
  - [`SlimReadOnlyListWrapper<T>` #](#slimreadonlylistwrappert-)

# インターフェース
## `INotifyArrayChanged` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/INotifyArrayChanged.cs#L11)
```csharp
public interface INotifyArrayChanged
```

## `IWeakList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/IWeakList.cs#L12)
```csharp
public interface IWeakList<T>
    where T : class
```

# クラス
## `FuncEqualityComparer<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/FuncEqualityComparer.cs#L11)
```csharp
public class FuncEqualityComparer<T> : IEqualityComparer<T>
```

## `LazyList<TSource, TTarget>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/LazyList.cs#L16)
```csharp
public class LazyList<TSource, TTarget> : IReadOnlyList<TTarget>
```

## `LockedWeakList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/LockedWeakList.cs#L14)
```csharp
public class LockedWeakList<T> : IWeakList<T>, IEnumerable<T>
    where T : class
```

## `ObservableArray<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/ObservableArray.cs#L17)
```csharp
public class ObservableArray<T> : IReadOnlyList<T>, IEquatable<ObservableArray<T>>, INotifyArrayChanged
```

## `SortedList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/SortedList.cs#L15)
```csharp
public class SortedList<T> : ICollection<T>, IReadOnlyList<T>, ISerializableSortedList
```

## `WeakList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/WeakList.cs#L14)
```csharp
public partial class WeakList<T> : IWeakList<T>, IEnumerable<T>
    where T : class
```

## `WeakList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/WeakList_ValidItemsEnumerator.cs#L9)
```csharp
public partial class WeakList<T>
```





# 構造体
## `SlimReadOnlyListWrapper<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Lists/SlimReadOnlyListWrapper.cs#L16)
```csharp
public readonly struct SlimReadOnlyListWrapper<T> : IList<T>, IList, IReadOnlyList<T>
```