- [Interface IStateful #](#interface-istateful-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Events](#events)
    - [StateChanged](#statechanged)
      - [Declaration](#declaration)
      - [Type](#type)
  - [Properties](#properties)
    - [State](#state)
      - [Declaration](#declaration-1)
      - [Type](#type-1)


# Interface IStateful<T> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IStateful.cs#L12)
状態を持ち、外部コンシューマが現在の状態を変更できるようにするオブジェクト。


## Namespace
osu.Framework


## Syntax
```csharp
public interface IStateful<T>
    where T : struct
```

## Events
### StateChanged
この[IStateful\<T\>]()の状態が変化したときに呼び出される。
#### Declaration
```csharp
event Action<T> StateChanged;
```
#### Type
|Name|Description|
|:-|:-|
|[Action\<T\>]()||


## Properties
### State
このオブジェクトの現在の状態。
#### Declaration
```csharp
T State { get; set; }
```
#### Type
|Name|Description|
|:-|:-|
|T|通常、このインターフェイスを実装するクラスに対してローカルな列挙型。|