# osu-framework interface Doc
- [osu-framework interface Doc](#osu-framework-interface-doc)
- [osu.Framework.Allocation](#osuframeworkallocation)
  - [public interface `IDependencyActivatorRegistry`](#public-interface-idependencyactivatorregistry)
    - [Method](#method)
  - [public interface `IDependencyInjectionCandidate`](#public-interface-idependencyinjectioncandidate)
  - [public interface `IReadOnlyDependencyContainer`](#public-interface-ireadonlydependencycontainer)
    - [Method](#method-1)
  - [public static `ReadonlyDependencyContainerExtensions`](#public-static-readonlydependencycontainerextensions)
    - [Method](#method-2)
  - [public interface `ISourceGenerateDependencyActivator`](#public-interface-isourcegeneratedependencyactivator)
    - [Method](#method-3)
  - [public interface `ISourceGeneratedLongRunningLoadCache`](#public-interface-isourcegeneratedlongrunningloadcache)
- [osu.Framework.Audio.Callbacks](#osuframeworkaudiocallbacks)
  - [public interface `IFileProcedures`](#public-interface-ifileprocedures)
    - [Method](#method-4)
- [osu.Framework.Audio.Mixing](#osuframeworkaudiomixing)
  - [public interface `IAudioChannel`](#public-interface-iaudiochannel)
    - [Property](#property)
  - [public interface `IAudioMixer`](#public-interface-iaudiomixer)
    - [Property](#property-1)
    - [Method](#method-5)
- [osu.Framework.Audio.Track](#osuframeworkaudiotrack)
  - [public interface `ITrack` : IAdjustableClock, IHasAmplitudes, IAdjustableAudioComponent](#public-interface-itrack--iadjustableclock-ihasamplitudes-iadjustableaudiocomponent)
    - [Property](#property-2)
    - [Method](#method-6)
  - [public interface `ITrackStore` : IAdjustableResourceStore\<Track\>](#public-interface-itrackstore--iadjustableresourcestoretrack)
    - [Method](#method-7)

# osu.Framework.Allocation
## public interface `IDependencyActivatorRegistry`
依存関係アクティブ化関数を登録するためのオブジェクトのインターフェイス。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IDependencyActivator.cs)
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`IsRegistered`|Type type|bool|依存関係アクティブ化関数が指定されたタイプに対してすでに登録されているかどうか。|
|`Register`|Type type, InjectDependencyDelegate? injectDel, CacheDependencyDelegate? cacheDel|void|指定された型の依存関係アクティブ化関数を登録する。|

## public interface `IDependencyInjectionCandidate`
[DependencyContainer.Inject{T}]()でオブジェクトを使用できるようにするためにオブジェクトにアタッチされるインターフェース。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/DependencyContainer.cs)

## public interface `IReadOnlyDependencyContainer`
型に基づいて依存関係を注入および取得できる依存関係コンテナへの読み取り専用インターフェース。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IReadOnlyDependencyContainer.cs)
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`Get`|Type type|object|"type"のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。|
|`Get`|Type type, CacheInfo info|object|"type"のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。|
|`Inject<T>`|T instance where T : class, IDependencyInjectionCandidate|void|指定されたインスタンスに依存関係を注入する。|

## public static `ReadonlyDependencyContainerExtensions`
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IReadOnlyDependencyContainer.cs)
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`Get<T>`|IReadOnlyDependencyContainer container|T|"T"型のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。|
|`Get<T>`|IReadOnlyDependencyContainer container, CacheInfo info|T|"T"型のキャッシュされた依存関係が存在する場合はそれを取得し、存在しない場合は null を取得する。|
|static `TryGet<T>`|IReadOnlyDependencyContainer container, out T value where T : class|bool|"T"型のキャッシュされた依存関係の取得を試みる。|
|static `TryGet<T>`|IReadOnlyDependencyContainer container, out T value where T : class, CacheInfo info|bool|"T"型のキャッシュされた依存関係の取得を試みる。|

## public interface `ISourceGenerateDependencyActivator`
依存関係をオブジェクトに注入するためにソースジェネレーターによって実装される。
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ISourceGeneratedDependencyActivator.cs)
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`RegisterForDependencyActivation`|IDependencyActivatorRegistry registry|void|このオブジェクトの依存関係アクティブ化関数を登録するために呼び出される。|

## public interface `ISourceGeneratedLongRunningLoadCache`
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ISourceGeneratedLongRunningLoadCache.cs)


# osu.Framework.Audio.Callbacks
## public interface `IFileProcedures`
[FileProcedures]()構造体の定義と厳密に一致するインターフェース。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/IFileProcedures.cs)
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`Length`|IntPtr user|long||
|`Close`|IntPtr user|void||
|`Seek`|long offset, IntPtr user|bool||
|`Read`|IntPtr buffer, int length, IntPtr user|int||


# osu.Framework.Audio.Mixing
## public interface `IAudioChannel`
オーディオを再生するオーディオチャネル。オーディオチャンネルは、[IAudioMixer.Add](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioMixer.cs)を介して別のミキサーにルーティングできる。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioChannel.cs)
### Property
|name|type|access|usage|
|:-|:-|:-|:-|
|`Name`|string|g|このサンプルを内部的に識別する名前。|

## public interface `IAudioMixer`
1 つ以上の[IAudioChannel](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioChannel.cs)をルーティングできるオーディオ ミキサー。他の[IAudioMixer](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioMixer.cs)から独立した DSP エフェクトをサポートする。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Mixing/IAudioMixer.cs)
### Property
|name|type|access|usage|
|:-|:-|:-|:-|
|`Effects`|BindableList\<IEffectParameter\>|g|現在ミックスに適用されているエフェクト。|
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`Add`|IAudioChannel channel|void|チャンネルをミックスに追加する。|
|`Remove`|IAudioChannel channel|void|ミックスからチャンネルを削除する。|


# osu.Framework.Audio.Track
## public interface `ITrack` : IAdjustableClock, IHasAmplitudes, IAdjustableAudioComponent
オーディオトラック。<br>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ITrack.cs)
### Property
|name|type|access|usage|
|:-|:-|:-|:-|
|event `Completed`|Action||このトラックが完了すると呼び出される。|
|event `Failed`|Action||このトラックが失敗したときに呼び出される。|
|`Looping`|bool||このトラックを繰り返すかどうかを示す。|
|`IsDummyDevice`|bool|g|このトラックはオーディオを生成できるか?|
|`RestartPoint`|double||ループまたは[Restart](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ITrack.cs)でトラックを再開する時点 (ミリ秒単位)。|
|`Length`|double||トラックの長さ (ミリ秒単位)。|
|`Bitrate`|int?|g|このトラックのビットレート。|
|`IsReversed`|bool|g|このトラックが逆向きかどうか。|
|`HasCompleted`|bool|g|このトラックの再生が終了したかどうか。|
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`Restart`||void|調整を保持したまま、このトラックを[Track.RestartPoint](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ITrack.cs)から再開する。|

## public interface `ITrackStore` : IAdjustableResourceStore\<Track\>
[ref](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/ITrackStore.cs)
### Method
|name|argument|return|usage|
|:-|:-|:-|:-|
|`GetVirtual`|double length=double.PositiveInfinity, string name="virtual"|Track|オーディオ デバイスのバックアップなしで[TrackVirtual](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Track/TrackVirtual.cs)を取得します。|


