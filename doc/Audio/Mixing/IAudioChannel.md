- [Interface IAudioChannel #](#interface-iaudiochannel-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Properties](#properties)
    - [Name](#name)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
    - [Mixer](#mixer)
      - [Declaration](#declaration-1)
      - [Type](#type)
  - [Methods](#methods)
    - [EnqueueAction](#enqueueaction)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-1)
      - [Return](#return)



# Interface IAudioChannel [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioChannel.cs#L12)
オーディオを再生するオーディオチャンネル。オーディオチャンネルは、[IAudioMixer.Add]()を介して別のミキサーにルーティングできる。


## Namespace
osu.Framework.Audio.Mixing


## Syntax
```csharp
public interface IAudioChannel
```


## Properties

### Name
このサンプルを内部的に識別する名前。
#### Declaration
```csharp
string Name { get; }
```
#### Arguments
|Type|Description|
|:-|:-|
|string||

### Mixer
このチャンネルによって生成されたすべてのオーディオがルーティングされるミキサー。
#### Declaration
```csharp
internal AudioMixer? Mixer { get; set; }
```
#### Type
|Type|Description|
|:-|:-|
|[AudioMixer]()||


## Methods

### EnqueueAction
このチャネルの一部としてオーディオ スレッドで実行されるアクションをキューに入れる。
#### Declaration
```csharp
internal Task EnqueueAction(Action action);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`action`|[Action]()|実行するアクション。|
#### Return
|Type|Description|
|:-|:-|
|[Task]()|継続ロジックに使用できるタスク。すでにオーディオスレッド上で呼び出された場合は、[Task.CompletedTask]()を返す場合がある。|