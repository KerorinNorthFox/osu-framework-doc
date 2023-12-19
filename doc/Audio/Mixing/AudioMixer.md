- [Class AudioMixer #](#class-audiomixer-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Properties](#properties)
    - [Identifier](#identifier)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [Effects](#effects)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
  - [Methods](#methods)
    - [Add](#add)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-1)
    - [Remove](#remove)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-2)
    - [Remove](#remove-1)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-3)
    - [AddInternal](#addinternal)
      - [Declaration](#declaration-6)
      - [Arguments](#arguments-4)
    - [RemoveInternal](#removeinternal)
      - [Declaration](#declaration-7)
      - [Arguments](#arguments-5)



# Class AudioMixer [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/AudioMixer.cs#L13)
複数の[IAudioChannel]()を1つの出力にミックスする。


## Namespace
osu.Framework.Audio.Mixing


## Implements
[AudioComponent]()<br>
[IAudioMixer]()


## Syntax
```csharp
public abstract class AudioMixer : AudioComponent, IAudioMixer
```


## Constructor
新しい[AudioMixer]()を作成する。
#### Declaration
```csharp
protected AudioMixer(AudioMixer? globalMixer, string identifier)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`globalMixer`|[AudioMixer]()|グローバルな[AudioMixer]()。[IAudioChannel]()がこのグローバルから削除された場合に移動される。<br>`null`値は、これがグローバル[AudioMixer]()であることを示す。|
|`identifier`|string|オーディオミキサービジュアライザーに表示される識別子。|


## Properties

### Identifier
#### Declaration
```csharp
public readonly string Identifier;
```
#### Type
|Type|Description|
|:-|:-|
|string||

### Effects
#### Declaration
```csharp
public abstract BindableList<IEffectParameter> Effects { get; }
```
#### Type
|Type|Description|
|:-|:-|
|[BindableList]()\<[IEffectParameter]()\>||


## Methods

### Add
#### Declaration
```csharp
public void Add(IAudioChannel channel)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()||

### Remove
[IAudioChannel]()をミックスから削除する。
#### Declaration
```csharp
public void Remove(IAudioChannel channel) => Remove(channel, true);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()||

### Remove
[IAudioChannel]()をミックスから削除する。
#### Declaration
```csharp
protected void Remove(IAudioChannel channel, bool returnToDefault)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()|削除する[IAudioChannel]()|
|`returnToDefault`|bool|`channel`をデフォルトのミキサーに戻すかどうか。|

### AddInternal
[IAudioChannel]()をミックスに追加する。
#### Declaration
```csharp
protected abstract void AddInternal(IAudioChannel channel);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()|追加する[IAudioChannel]() 。|

### RemoveInternal
[IAudioChannel]()をミックスから削除する。
#### Declaration
```csharp
protected abstract void RemoveInternal(IAudioChannel channel);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`channel`|[IAudioChannel]()|削除する[IAudioChannel]() 。|