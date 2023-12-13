- [Property](#property)
  - [Game.Window](#gamewindow)
    - [Type](#type)
  - [Game.Resources](#gameresources)
    - [Type](#type-1)
  - [Game.Textures](#gametextures)
    - [Type](#type-2)
  - [Game.DefaultTextureFilteringMode](#gamedefaulttexturefilteringmode)
    - [Type](#type-3)
  - [Game.Host](#gamehost)
    - [Type](#type-4)
  - [Game.IsActive](#gameisactive)
    - [Type](#type-5)
  - [Game.Audio](#gameaudio)
    - [Type](#type-6)
  - [Game.Shaders](#gameshaders)
    - [Type](#type-7)
  - [Game.Fonts](#gamefonts)
    - [Type](#type-8)
  - [Game.Localisation](#gamelocalisation)
    - [Type](#type-9)
  - [Game.Content](#gamecontent)
    - [Type](#type-10)
  - [Game.FrameStatistics](#gameframestatistics)
- [Method](#method)
  - [Game.CreateLocalisationManager](#gamecreatelocalisationmanager)
    - [Arguments](#arguments)
    - [Return](#return)
  - [Game.CreateUserInputManager](#gamecreateuserinputmanager)
    - [Return](#return-1)
  - [Game.GetFrameworkConfigDefaults](#gamegetframeworkconfigdefaults)
    - [Return](#return-2)
  - [Game.CreateStorage](#gamecreatestorage)
    - [Arguments](#arguments-1)
    - [Return](#return-3)
  - [Game.SetHost](#gamesethost)
    - [Arguments](#arguments-2)
  - [Game.CreateChildDependencies](#gamecreatechilddependencies)
    - [Arguments](#arguments-3)
    - [Return](#return-4)
  - [Game.AddFont](#gameaddfont)
    - [Arguments](#arguments-4)
  - [Game.LoadComplete](#gameloadcomplete)
  - [Game.OnPressed](#gameonpressed)
    - [Arguments](#arguments-5)
    - [Return](#return-5)
  - [Game.CycleFrameStatistics](#gamecycleframestatistics)
  - [Game.OnReleased](#gameonreleased)
    - [Arguments](#arguments-6)
  - [Game.OnPressed](#gameonpressed-1)
    - [Arguments](#arguments-7)
    - [Return](#return-6)
  - [Game.OnReleased](#gameonreleased-1)
    - [Arguments](#arguments-8)
  - [Game.RequestExit](#gamerequestexit)
  - [Game.Exit](#gameexit)
  - [Game.OnExiting](#gameonexiting)
    - [Return](#return-7)
  - [Game.Dispose](#gamedispose)
    - [Arguments](#arguments-9)

# Property
## Game[.Window](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L33)
```csharp
public IWindow Window => Host?.Window;
```
### Type
|Name|Description|
|:-|:-|
|[IWindow](/osu-framework-doc/doc/Platform/README.md#iwindow)|ゲーム ウィンドウのインターフェイス表現。実装固有のコードを隠すことを目的としている。|

## Game[.Resources](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L35)
```csharp
public ResourceStore<byte[]> Resources { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[ResourceStore\<byte[]\>](/osu-framework-doc/doc/IO/Stores/README.md#resourcestoret)||

## Game[.Textures](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L37)
```csharp
public TextureStore Textures { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[TextureStore]()||

## Game[.DefaultTextureFilteringMode](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L42)
[Textures]()からフェッチされたすべてのテクスチャに使用するフィルタリング モード。
```csharp
protected virtual TextureFilteringMode DefaultTextureFilteringMode => TextureFilteringMode.Linear;
```
### Type
|Name|Description|
|:-|:-|
|[TextureFilteringMode]()||

## Game[.Host](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L44)
```csharp
protected GameHost Host { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[GameHost]()||

## Game[.IsActive](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L51)
ゲームがアクティブであるかどうか。(フォアグラウンドで)
```csharp
public IBindable<bool> IsActive => isActive;
```
### Type
|Name|Description|
|:-|:-|
|[IBindable\<bool\>]()||

## Game[.Audio](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L53)
```csharp
public AudioManager Audio { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[AudioManager]()||

## Game[.Shaders](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L55)
```csharp
public ShaderManager Shaders { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[ShaderManager]()||

## Game[.Fonts](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L63)
ゲーム全体でアクセスできるフォントを含むストア。<br>
新しいフォントを追加するときは、[AddFont]()を使用することをお勧めする。
```csharp
public FontStore Fonts { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[FontStore]()||

## Game[.Localisation](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L67)
```csharp
protected LocalisationManager Localisation { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[LocalisationManager]()||

## Game[.Content](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L81)
```csharp
protected override Container<Drawable> Content => content;
```
### Type
|Name|Description|
|:-|:-|
|[Container\<Drawable\>]()||

## Game[.FrameStatistics](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L282)
```csharp
protected readonly Bindable<FrameStatisticsMode> FrameStatistics = new Bindable<FrameStatisticsMode>();
```


# Method
## Game[.CreateLocalisationManager](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L87)
新しい[LocalisationManager]()を作成する。
```csharp
protected virtual LocalisationManager CreateLocalisationManager(FrameworkConfigManager frameworkConfig) => new LocalisationManager(frameworkConfig);
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`frameworkConfig`|[FrameworkConfigManager]()|フレームワーク構成マネージャー。|
### Return
|Type|Description|
|:-|:-|
|[LocalisationManager]()||

## Game[.CreateUserInputManager](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L89)
```csharp
protected internal virtual UserInputManager CreateUserInputManager() => new UserInputManager();
```
### Return
|Type|Description|
|:-|:-|
|[UserInputManager]()||

## Game[.GetFrameworkConfigDefaults](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L97)
osu-framework によって提供されるデフォルトをオーバーライドする必要がある[FrameworkSetting]()デフォルトを提供する。<br>
予想される型については、[こちら](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameworkConfigManager.cs)を確認。
```csharp
protected internal virtual IDictionary<FrameworkSetting, object> GetFrameworkConfigDefaults() => null;
```
### Return
|Type|Description|
|:-|:-|
|[IDictionary<FrameworkSetting, object>]()||

## Game[.CreateStorage](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L105)
この[Game]()が存在する[Storage]()を作成する。
```csharp
protected internal virtual Storage CreateStorage(GameHost host, Storage defaultStorage) => defaultStorage;
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`host`|[GameHost]()|[GameHost]()参照|
|`defaultStorage`|[Storage]()|カスタム[Storage]()が必要ない場合に使用されるデフォルトの[Storage]()。|
### Return
|Type|Description|
|:-|:-|
|[Storage]()|[Storage]()参照|

## Game[.SetHost](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L135)
Load はホストの作成後に実行されるため、このメソッドをオーバーライドして、ホスト自体がユーザーに表示される前にホストのプロパティを変更できる。
```csharp
public virtual void SetHost(GameHost host)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`host`|[GameHost]()||

## Game[.CreateChildDependencies](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L145)
```csharp
protected override IReadOnlyDependencyContainer CreateChildDependencies(IReadOnlyDependencyContainer parent) =>
    dependencies = new DependencyContainer(base.CreateChildDependencies(parent));
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`parent`|[IReadOnlyDependencyContainer]()||
### Return
|Type|Description|
|:-|:-|
|[IReadOnlyDependencyContainer]()||

## Game[.AddFont](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L243)
ゲームにグローバルにアクセスできるようにフォントを追加する。
```csharp
public void AddFont(ResourceStore<byte[]> store, string assetName = null, FontStore target = null)
    => addFont(target ?? Fonts, store, assetName);
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`store`|[ResourceStore<byte[]>]()|フォントリソースを含むバッキングストア。|
|`assetName` = null|string|フォントのベース名。|
|`target` = null|[FontStore]()|フォントを追加するオプションのターゲットストア。指定しない場合は、[Fonts]()が使用される。|

## Game[.LoadComplete](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L249)
```csharp
protected override void LoadComplete()
```

## Game[.OnPressed](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L294)
```csharp
public bool OnPressed(KeyBindingPressEvent<FrameworkAction> e)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingPressEvent\<FrameworkAction\>]()||
### Return
|Type|Description|
|:-|:-|
|bool||

## Game[.CycleFrameStatistics](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L401)
```csharp
protected void CycleFrameStatistics()
```

## Game[.OnReleased](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L429)
```csharp
public void OnReleased(KeyBindingReleaseEvent<FrameworkAction> e)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingReleaseEvent\<FrameworkAction\>]()||

## Game[.OnPressed](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L433)
```csharp
public virtual bool OnPressed(KeyBindingPressEvent<PlatformAction> e)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingPressEvent\<PlatformAction\>]()||
### Return
|Type|Description|
|:-|:-|
|bool||

## Game[.OnReleased](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L448)
```csharp
public virtual void OnReleased(KeyBindingReleaseEvent<PlatformAction> e)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingReleaseEvent\<PlatformAction\>]()||

## Game[.RequestExit](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L455)
ゲームの終了を要求する。この終了は、[OnExiting]()によってブロックできる。
```csharp
public void RequestExit()
```

## Game[.Exit](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L464)
[OnExiting]()戻り値を無視して、ゲームを強制終了する。
```csharp
public void Exit()
```

## Game[.OnExiting](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L477)
終了が要求されたときに発生する。<br>
通常、[PlatformAction.Exit]()またはウィンドウを閉じる(X)ボタンが押されたときに発生する。<br>
終了プロセスをブロックするには、`true`を返す。
```csharp
protected virtual bool OnExiting() => false;
```
### Return
|Type|Description|
|:-|:-|
|bool||

## Game[.Dispose](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L479)
```csharp
protected override void Dispose(bool isDisposing)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`isDisposing`|bool||