- [Event](#event)
  - [IStateful.StateChanged](#istatefulstatechanged)
    - [Type](#type)
- [Property](#property)
  - [IStateful.State](#istatefulstate)
    - [Type](#type-1)

# Event
## IStateful[.StateChanged](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IStateful.cs#L18)
この[IStateful\<T\>]()の状態が変化したときに呼び出される。
```csharp
event Action<T> StateChanged;
```
### Type
|Name|Description|
|:-|:-|
|[Action\<T\>]()||

# Property
## IStateful[.State](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IStateful.cs#L23)
このオブジェクトの現在の状態。
```csharp
T State { get; set; }
```
### Type
|Name|Description|
|:-|:-|
|T|通常、このインターフェイスを実装するクラスに対してローカルな列挙型。|