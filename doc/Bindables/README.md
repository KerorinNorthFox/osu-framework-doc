# osu.Framework.Bindables Doc
- [osu.Framework.Bindables Doc](#osuframeworkbindables-doc)
- [インターフェース](#インターフェース)
  - [`IBindable` #](#ibindable-)
  - [`IBindable<T>` #](#ibindablet-)
  - [`IBindableDictionary<TKey, TValue>` #](#ibindabledictionarytkey-tvalue-)
  - [`IBindableList<T>` #](#ibindablelistt-)
  - [`IBindableNumber<T>` #](#ibindablenumbert-)
  - [`IBindableWithCurrent<T>` #](#ibindablewithcurrentt-)
  - [`ICanBeDisabled` #](#icanbedisabled-)
  - [`IHasDefaultValue` #](#ihasdefaultvalue-)
  - [`IHasDescription` #](#ihasdescription-)
  - [`ILeasedBindable` #](#ileasedbindable-)
  - [`ILeasedBindable<T>` #](#ileasedbindablet-)
  - [`IParseable` #](#iparseable-)
  - [`IUnbindable` #](#iunbindable-)
- [クラス](#クラス)
  - [`AggregateBindable<T>` #](#aggregatebindablet-)
  - [`Bindable<T>` #](#bindablet-)
  - [`BindableBool` #](#bindablebool-)
  - [`BindableColour4` #](#bindablecolour4-)
  - [`BindableDictionary<TKey, TValue>` #](#bindabledictionarytkey-tvalue-)
  - [`BindableDouble` #](#bindabledouble-)
  - [`BindableFloat` #](#bindablefloat-)
  - [`BindableInt` #](#bindableint-)
  - [`BindableList<T>` #](#bindablelistt-)
  - [`BindableLong` #](#bindablelong-)
  - [`BindableMarginPadding` #](#bindablemarginpadding-)
  - [`BindableNumber<T>` #](#bindablenumbert-)
  - [`BindableNumberWithCurrent<T>` #](#bindablenumberwithcurrentt-)
  - [`BindableSafeArea` #](#bindablesafearea-)
  - [`BindableSize` #](#bindablesize-)
  - [`BindableWithCurrent<T>` #](#bindablewithcurrentt-)
  - [`LeasedBindable<T>` #](#leasedbindablet-)
  - [`NonNullableBindable<T>` #](#nonnullablebindablet-)
  - [`NotifyDictionaryChangedEventArgs<TKey, TValue>` #](#notifydictionarychangedeventargstkey-tvalue-)
  - [`RangeConstrainedBindable<T>` #](#rangeconstrainedbindablet-)
  - [`ValueChangedEvent<T>` #](#valuechangedeventt-)
- [列挙型](#列挙型)
  - [`NotifyDictionaryChangedAction` #](#notifydictionarychangedaction-)
- [デリゲート](#デリゲート)
  - [`NotifyDictionaryChangedEventHandler<TKey, TValue>` #](#notifydictionarychangedeventhandlertkey-tvalue-)


# インターフェース
## `IBindable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IBindable.cs#L15)
```csharp
public interface IBindable : ICanBeDisabled, IHasDefaultValue, IUnbindable, IHasDescription, IFormattable
```

## `IBindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IBindable.cs#L73)
```csharp
public interface IBindable<T> : ICanBeDisabled, IHasDefaultValue, IUnbindable, IHasDescription, IFormattable
```

## `IBindableDictionary<TKey, TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IBindableDictionary.cs#L8)
```csharp
public interface IBindableDictionary<TKey, TValue> : IReadOnlyDictionary<TKey, TValue>, ICanBeDisabled, IHasDefaultValue, IUnbindable, IHasDescription
        where TKey : notnull
```

## `IBindableList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IBindableList.cs#L13)
```csharp
public interface IBindableList<T> : IReadOnlyList<T>, ICanBeDisabled, IHasDefaultValue, IUnbindable, IHasDescription, INotifyCollectionChanged
```

## `IBindableNumber<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IBindableNumber.cs#L8)
```csharp
public interface IBindableNumber<T> : IBindable<T>
        where T : struct, IComparable<T>, IEquatable<T>
```

## `IBindableWithCurrent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IBindableWithCurrent.cs#L12)
```csharp
public interface IBindableWithCurrent<T> : IBindable<T>, IHasCurrentValue<T>
```

## `ICanBeDisabled` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/ICanBeDisabled.cs#L11)
```csharp
public interface ICanBeDisabled
```

## `IHasDefaultValue` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IHasDefaultValue.cs#L9)
```csharp
public interface IHasDefaultValue
```

## `IHasDescription` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IHasDescription.cs#L11)
```csharp
public interface IHasDescription
```

## `ILeasedBindable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/ILeasedBindable.cs#L9)
```csharp
public interface ILeasedBindable : IBindable
```

## `ILeasedBindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/ILeasedBindable.cs#L24)
```csharp
public interface ILeasedBindable<T> : ILeasedBindable, IBindable<T>
```

## `IParseable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IParseable.cs#L9)
```csharp
public interface IParseable
```

## `IUnbindable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/IUnbindable.cs#L9)
```csharp
public interface IUnbindable
```






# クラス
## `AggregateBindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/AggregateBindable.cs#L16)
```csharp
public class AggregateBindable<T>
```

## `Bindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/Bindable.cs#L23)
```csharp
public class Bindable<T> : IBindable<T>, IBindable, IParseable, ISerializableBindable
```

## `BindableBool` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableBool.cs#L8)
```csharp
public class BindableBool : Bindable<bool>
```

## `BindableColour4` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableColour4.cs#L9)
```csharp
public class BindableColour4 : Bindable<Colour4>
```

## `BindableDictionary<TKey, TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableDictionary.cs#L17)
```csharp
public class BindableDictionary<TKey, TValue> : IBindableDictionary<TKey, TValue>, IBindable, IParseable, IDictionary<TKey, TValue>, IDictionary
        where TKey : notnull
```

## `BindableDouble` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableDouble.cs#L8)
```csharp
public class BindableDouble : BindableNumber<double>
```
## `BindableFloat` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableFloat.cs#L8)
```csharp
public class BindableFloat : BindableNumber<float>
```

## `BindableInt` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableInt.cs#L6)
```csharp
public class BindableInt : BindableNumber<int>
```

## `BindableList<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableList.cs#L18)
```csharp
public class BindableList<T> : IBindableList<T>, IBindable, IParseable, IList<T>, IList
```

## `BindableLong` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableLong.cs#L6)
```csharp
public class BindableLong : BindableNumber<long>
```

## `BindableMarginPadding` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableMarginPadding.cs#L10)
```csharp
public class BindableMarginPadding : RangeConstrainedBindable<MarginPadding>
```

## `BindableNumber<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableNumber.cs#L13)
```csharp
public class BindableNumber<T> : RangeConstrainedBindable<T>, IBindableNumber<T>
        where T : struct, IComparable<T>, IConvertible, IEquatable<T>
```

## `BindableNumberWithCurrent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableNumberWithCurrent.cs#L14)
```csharp
public class BindableNumberWithCurrent<T> : BindableNumber<T>, IBindableWithCurrent<T>
        where T : struct, IComparable<T>, IConvertible, IEquatable<T>
```

## `BindableSafeArea` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableSafeArea.cs#L12)
```csharp
public class BindableSafeArea : Bindable<MarginPadding>
```

## `BindableSize` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableSize.cs#L12)
```csharp
public class BindableSize : RangeConstrainedBindable<Size>
```

## `BindableWithCurrent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/BindableWithCurrent.cs#L14)
```csharp
public class BindableWithCurrent<T> : Bindable<T>, IBindableWithCurrent<T>
```

## `LeasedBindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/LeasedBindable.cs#L17)
```csharp
public class LeasedBindable<T> : Bindable<T>, ILeasedBindable<T>
```

## `NonNullableBindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/NonNullableBindable.cs#L8)
```csharp
public class NonNullableBindable<T> : Bindable<T>
```

## `NotifyDictionaryChangedEventArgs<TKey, TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/NotifyDictionaryChangedEventArgs.cs#L14)
```csharp
public class NotifyDictionaryChangedEventArgs<TKey, TValue> : EventArgs
        where TKey : notnull
```

## `RangeConstrainedBindable<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/RangeConstrainedBindable.cs#L11)
```csharp
public abstract class RangeConstrainedBindable<T> : Bindable<T>
```

## `ValueChangedEvent<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/ValueChangedEvent.cs#L10)
```csharp
public class ValueChangedEvent<T>
```







# 列挙型
## `NotifyDictionaryChangedAction` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/NotifyDictionaryChangedEventArgs.cs#L85)
```csharp
public enum NotifyDictionaryChangedAction
```





# デリゲート
## `NotifyDictionaryChangedEventHandler<TKey, TValue>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Bindables/NotifyDictionaryChangedEventArgs.cs#L82)
```csharp
public delegate void NotifyDictionaryChangedEventHandler<TKey, TValue>(object? sender, NotifyDictionaryChangedEventArgs<TKey, TValue> e)
        where TKey : notnull;
```



