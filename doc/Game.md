# Property
## Game[.Window](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L33)
```csharp
public IWindow Window => Host?.Window;
```
### Type
|Name|Description|
|:-|:-|
|[IWindow](/osu-framework-doc/doc/Platform/README.md#iwindow)|ゲーム ウィンドウのインターフェイス表現。実装固有のコードを隠すことを目的としている。|
### Access
使用

## Game[.Resources](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L35)
```csharp
public ResourceStore<byte[]> Resources { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[ResourceStore\<byte[]\>](/osu-framework-doc/doc/IO/Stores/README.md#resourcestoret)||
### Access
使用

## Game[.Textures](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L37)
```csharp
public TextureStore Textures { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[TextureStore]()||
### Access
使用

## Game[.DefaultTextureFilteringMode](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L42)
[Textures]()からフェッチされたすべてのテクスチャに使用するフィルタリング モード。
```csharp
protected virtual TextureFilteringMode DefaultTextureFilteringMode => TextureFilteringMode.Linear;
```
### Type
|Name|Description|
|:-|:-|
|[TextureFilteringMode]()||
### Access
継承先で使用かオーバーライドして使用

## Game[.IsActive](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L51)
ゲームがアクティブであるかどうか。(フォアグラウンドで)
```csharp
public IBindable<bool> IsActive => isActive;
```
### Type
|Name|Description|
|:-|:-|
|[IBindable\<bool\>]()||
### Access
使用

## Game[.Audio](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L53)
```csharp
public AudioManager Audio { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[AudioManager]()||
### Access
使用

## Game[.Shaders](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L55)
```csharp
public ShaderManager Shaders { get; private set; }
```
### Type
|Name|Description|
|:-|:-|
|[ShaderManager]()||
### Access
使用

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
### Access
使用


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
### Access
継承先で使用かオーバーライドして使用

## Game[.CreateUserInputManager](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L89)
```csharp
protected internal virtual UserInputManager CreateUserInputManager() => new UserInputManager();
```
### Return
|Type|Description|
|:-|:-|
|[UserInputManager]()||
### Access
継承先で使用かオーバーライドして使用

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
### Access
継承先で使用かオーバーライドして使用

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
### Access
継承先で使用かオーバーライドして使用

## Game[.SetHost](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L135)
Load はホストの作成後に実行されるため、このメソッドをオーバーライドして、ホスト自体がユーザーに表示される前にホストのプロパティを変更できる。
```csharp
public virtual void SetHost(GameHost host)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`host`|[GameHost]()||
### Access
使用かオーバーライドして使用

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
### Access
使用

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
### Access
使用

## Game[.OnReleased](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L429)
```csharp
public void OnReleased(KeyBindingReleaseEvent<FrameworkAction> e)
```
### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`e`|[KeyBindingReleaseEvent\<FrameworkAction\>]()||
### Access
使用

TODO: protectedなプロパティやメソッドもdocに含め、Accessは「継承して使用」にする