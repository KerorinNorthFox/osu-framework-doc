- [Class Game #](#class-game-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Properties](#properties)
    - [Window](#window)
      - [Declaration](#declaration)
      - [Type](#type)
    - [Resources](#resources)
      - [Declaration](#declaration-1)
      - [Type](#type-1)
    - [Textures](#textures)
      - [Declaration](#declaration-2)
      - [Type](#type-2)
    - [DefaultTextureFilteringMode](#defaulttexturefilteringmode)
      - [Declaration](#declaration-3)
      - [Type](#type-3)
    - [Host](#host)
      - [Declaration](#declaration-4)
      - [Type](#type-4)
    - [IsActive](#isactive)
      - [Declaration](#declaration-5)
      - [Type](#type-5)
    - [Audio](#audio)
      - [Declaration](#declaration-6)
      - [Type](#type-6)
    - [Shaders](#shaders)
      - [Declaration](#declaration-7)
      - [Type](#type-7)
    - [Fonts](#fonts)
      - [Declaration](#declaration-8)
      - [Type](#type-8)
    - [Localisation](#localisation)
      - [Declaration](#declaration-9)
      - [Type](#type-9)
    - [Content](#content)
      - [Declaration](#declaration-10)
      - [Type](#type-10)
    - [FrameStatistics](#framestatistics)
      - [Declaration](#declaration-11)
  - [Methods](#methods)
    - [CreateLocalisationManager](#createlocalisationmanager)
      - [Declaration](#declaration-12)
      - [Arguments](#arguments)
      - [Return](#return)
    - [CreateUserInputManager](#createuserinputmanager)
      - [Declaration](#declaration-13)
      - [Return](#return-1)
    - [GetFrameworkConfigDefaults](#getframeworkconfigdefaults)
      - [Declaration](#declaration-14)
      - [Return](#return-2)
    - [CreateStorage](#createstorage)
      - [Declaration](#declaration-15)
      - [Arguments](#arguments-1)
      - [Return](#return-3)
    - [SetHost](#sethost)
      - [Declaration](#declaration-16)
      - [Arguments](#arguments-2)
    - [CreateChildDependencies](#createchilddependencies)
      - [Declaration](#declaration-17)
      - [Arguments](#arguments-3)
      - [Return](#return-4)
    - [AddFont](#addfont)
      - [Declaration](#declaration-18)
      - [Arguments](#arguments-4)
    - [LoadComplete](#loadcomplete)
      - [Declaration](#declaration-19)
    - [OnPressed](#onpressed)
      - [Declaration](#declaration-20)
      - [Arguments](#arguments-5)
      - [Return](#return-5)
    - [CycleFrameStatistics](#cycleframestatistics)
      - [Declaration](#declaration-21)
    - [OnReleased](#onreleased)
      - [Declaration](#declaration-22)
      - [Arguments](#arguments-6)
    - [OnPressed](#onpressed-1)
      - [Declaration](#declaration-23)
      - [Arguments](#arguments-7)
      - [Return](#return-6)
    - [OnReleased](#onreleased-1)
      - [Declaration](#declaration-24)
      - [Arguments](#arguments-8)
    - [RequestExit](#requestexit)
      - [Declaration](#declaration-25)
    - [Exit](#exit)
      - [Declaration](#declaration-26)
    - [OnExiting](#onexiting)
      - [Declaration](#declaration-27)
      - [Return](#return-7)
    - [Dispose](#dispose)
      - [Declaration](#declaration-28)
      - [Arguments](#arguments-9)


# Class Game [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L31)


## Namespace
osu.Framework


## Implements
[Container]()<br>
[IKeyBindingHandler\<FrameworkAction\>]()<br>
[IKeyBindingHandler\<PlatformAction\>]()<br>
[IHandleGlobalKeyboardInput]()<br>


## Syntax
```csharp
public abstract partial class Game : Container, IKeyBindingHandler<FrameworkAction>, IKeyBindingHandler<PlatformAction>, IHandleGlobalKeyboardInput
```


## Properties

### Window
#### Declaration
```csharp
public IWindow Window => Host?.Window;
```
#### Type
|Name|Description|
|:-|:-|
|[IWindow]()|ゲーム ウィンドウのインターフェイス表現。実装固有のコードを隠すことを目的としている。|

---
### Resources
#### Declaration
```csharp
public ResourceStore<byte[]> Resources { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[ResourceStore\<byte[]\>]()||

---
### Textures
#### Declaration
```csharp
public TextureStore Textures { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[TextureStore]()||

---
### DefaultTextureFilteringMode
[Textures]()からフェッチされたすべてのテクスチャに使用するフィルタリング モード。
#### Declaration
```csharp
protected virtual TextureFilteringMode DefaultTextureFilteringMode => TextureFilteringMode.Linear;
```
#### Type
|Name|Description|
|:-|:-|
|[TextureFilteringMode]()||

---
### Host
#### Declaration
```csharp
protected GameHost Host { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[GameHost]()||

---
### IsActive
ゲームがアクティブであるかどうか。(フォアグラウンドで)
#### Declaration
```csharp
public IBindable<bool> IsActive => isActive;
```
#### Type
|Name|Description|
|:-|:-|
|[IBindable\<bool\>]()||

---
### Audio
#### Declaration
```csharp
public AudioManager Audio { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[AudioManager]()||

---
### Shaders
#### Declaration
```csharp
public ShaderManager Shaders { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[ShaderManager]()||

---
### Fonts
ゲーム全体でアクセスできるフォントを含むストア。<br>
新しいフォントを追加するときは、[AddFont]()を使用することをお勧めする。
#### Declaration
```csharp
public FontStore Fonts { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[FontStore]()||

---
### Localisation
#### Declaration
```csharp
protected LocalisationManager Localisation { get; private set; }
```
#### Type
|Name|Description|
|:-|:-|
|[LocalisationManager]()||

---
### Content
#### Declaration
```csharp
protected override Container<Drawable> Content => content;
```
#### Type
|Name|Description|
|:-|:-|
|[Container\<Drawable\>]()||

---
### FrameStatistics
#### Declaration
```csharp
protected readonly Bindable<FrameStatisticsMode> FrameStatistics = new Bindable<FrameStatisticsMode>();
```


## Methods

### CreateLocalisationManager
新しい[LocalisationManager]()を作成する。
#### Declaration
```csharp
protected virtual LocalisationManager CreateLocalisationManager(FrameworkConfigManager frameworkConfig) => new LocalisationManager(frameworkConfig);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`frameworkConfig`|[FrameworkConfigManager]()|フレームワーク構成マネージャー。|
#### Return
|Type|Description|
|:-|:-|
|[LocalisationManager]()||

---
### CreateUserInputManager
#### Declaration
```csharp
protected internal virtual UserInputManager CreateUserInputManager() => new UserInputManager();
```
#### Return
|Type|Description|
|:-|:-|
|[UserInputManager]()||

---
### GetFrameworkConfigDefaults
osu-framework によって提供されるデフォルトをオーバーライドする必要がある[FrameworkSetting]()デフォルトを提供する。<br>
予想される型については、[こちら](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Configuration/FrameworkConfigManager.cs)を確認。
#### Declaration
```csharp
protected internal virtual IDictionary<FrameworkSetting, object> GetFrameworkConfigDefaults() => null;
```
#### Return
|Type|Description|
|:-|:-|
|[IDictionary<FrameworkSetting, object>]()||

---
### CreateStorage
この[Game]()が存在する[Storage]()を作成する。
#### Declaration
```csharp
protected internal virtual Storage CreateStorage(GameHost host, Storage defaultStorage) => defaultStorage;
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`host`|[GameHost]()|[GameHost]()参照|
|`defaultStorage`|[Storage]()|カスタム[Storage]()が必要ない場合に使用されるデフォルトの[Storage]()。|
#### Return
|Type|Description|
|:-|:-|
|[Storage]()|[Storage]()参照|

---
### SetHost
Load はホストの作成後に実行されるため、このメソッドをオーバーライドして、ホスト自体がユーザーに表示される前にホストのプロパティを変更できる。
#### Declaration
```csharp
public virtual void SetHost(GameHost host)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`host`|[GameHost]()||

---
### CreateChildDependencies
#### Declaration
```csharp
protected override IReadOnlyDependencyContainer CreateChildDependencies(IReadOnlyDependencyContainer parent) =>
    dependencies = new DependencyContainer(base.CreateChildDependencies(parent));
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`parent`|[IReadOnlyDependencyContainer]()||
#### Return
|Type|Description|
|:-|:-|
|[IReadOnlyDependencyContainer]()||

---
### AddFont
ゲームにグローバルにアクセスできるようにフォントを追加する。
#### Declaration
```csharp
public void AddFont(ResourceStore<byte[]> store, string assetName = null, FontStore target = null)
    => addFont(target ?? Fonts, store, assetName);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`store`|[ResourceStore<byte[]>]()|フォントリソースを含むバッキングストア。|
|`assetName` = null|string|フォントのベース名。|
|`target` = null|[FontStore]()|フォントを追加するオプションのターゲットストア。指定しない場合は、[Fonts]()が使用される。|

---
### LoadComplete
#### Declaration
```csharp
protected override void LoadComplete()
```

---
### OnPressed
#### Declaration
```csharp
public bool OnPressed(KeyBindingPressEvent<FrameworkAction> e)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingPressEvent\<FrameworkAction\>]()||
#### Return
|Type|Description|
|:-|:-|
|bool||

---
### CycleFrameStatistics
#### Declaration
```csharp
protected void CycleFrameStatistics()
```

---
### OnReleased
#### Declaration
```csharp
public void OnReleased(KeyBindingReleaseEvent<FrameworkAction> e)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingReleaseEvent\<FrameworkAction\>]()||

---
### OnPressed
#### Declaration
```csharp
public virtual bool OnPressed(KeyBindingPressEvent<PlatformAction> e)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingPressEvent\<PlatformAction\>]()||
#### Return
|Type|Description|
|:-|:-|
|bool||

---
### OnReleased
#### Declaration
```csharp
public virtual void OnReleased(KeyBindingReleaseEvent<PlatformAction> e)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingReleaseEvent\<PlatformAction\>]()||

---
### RequestExit
ゲームの終了を要求する。この終了は、[OnExiting]()によってブロックできる。
#### Declaration
```csharp
public void RequestExit()
```

---
### Exit
[OnExiting]()戻り値を無視して、ゲームを強制終了する。
#### Declaration
```csharp
public void Exit()
```

---
### OnExiting
終了が要求されたときに発生する。<br>
通常、[PlatformAction.Exit]()またはウィンドウを閉じる(X)ボタンが押されたときに発生する。<br>
終了プロセスをブロックするには、`true`を返す。
#### Declaration
```csharp
protected virtual bool OnExiting() => false;
```
#### Return
|Type|Description|
|:-|:-|
|bool||

---
### Dispose
#### Declaration
```csharp
protected override void Dispose(bool isDisposing)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`isDisposing`|bool||