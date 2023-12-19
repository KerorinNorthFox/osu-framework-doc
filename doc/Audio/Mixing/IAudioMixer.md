- [Interface IAudioMixer #](#interface-iaudiomixer-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Properties](#properties)
    - [Effects](#effects)
      - [Declaration](#declaration)
      - [Type](#type)
  - [Methods](#methods)
    - [Add](#add)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments)
    - [Remove](#remove)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-1)



# Interface IAudioMixer [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioMixer.cs#L13)
1 つ以上の[IAudioChannel]()をルーティングできるオーディオミキサー。<br>
他の[IAudioMixer]()から独立した DSP エフェクトをサポートする。


## Namespace
osu.Framework.Audio.Mixing


## Syntax
```csharp
public interface IAudioMixer
```


## Properties

### Effects
現在ミックスに適用されているエフェクト。<br>
エフェクトは、リスト内の`index = 0`にあるエフェクトが最も高い優先度を持ち、リスト内の`index = Count - 1`にあるエフェクトが最も低い優先度を持つように、優先順位の降順に保存される。
#### Declaration
```csharp
BindableList<IEffectParameter> Effects { get; }
```
#### Type
|Type|Description|
|:-|:-|
|[BindableList]()\<[IEffectParameter]()\>||


## Methods

### Add
チャンネルをミックスに追加する。
#### Declaration
```csharp
void Add(IAudioChannel channel);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()|追加するチャンネル。|

### Remove
ミックスからチャンネルを削除する。
#### Declaration
```csharp
void Remove(IAudioChannel channel);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()|削除するチャンネル。|