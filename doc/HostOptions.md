- [Property](#property)
  - [HostOptions.BindIPC](#hostoptionsbindipc)
    - [Type](#type)
  - [HostOptions.PortableInstallation](#hostoptionsportableinstallation)
    - [Type](#type-1)
  - [HostOptions.BypassCompositor](#hostoptionsbypasscompositor)
    - [Type](#type-2)

# Property
## HostOptions[.BindIPC](https://github.com/ppy/osu-framework/blob/master/osu.Framework/HostOptions.cs#L16)
IPC ポートをバインドするかどうか。使用法の詳細については、[IIpcHost]()を参照。
```csharp
public bool BindIPC { get; set; }
```
### Type
|Name|Description|
|:-|:-|
|bool||

## HostOptions[.PortableInstallation](https://github.com/ppy/osu-framework/blob/master/osu.Framework/HostOptions.cs#L21)
これがポータブルインストールであるかどうか。すべてのゲーム ファイルは、標準のデータディレクトリではなく、実行可能ファイルと一緒に配置される。
```csharp
public bool PortableInstallation { get; set; }
```
### Type
|Name|Description|
|:-|:-|
|bool||

## HostOptions[.BypassCompositor](https://github.com/ppy/osu-framework/blob/master/osu.Framework/HostOptions.cs#L32)
コンポジターをバイパスするかどうか。デフォルトは`true`。<br>
Linux では、コンポジターはさまざまなウィンドウ効果を適用するためにアプリケーションを再バッファリングするため、プロセスのレイテンシーが増加する。したがって、ゲームではこれをバイパスするのが得策だが、普通のアプリケーションでは通常、ウィンドウの効果をそのままにしておく方が有益である。<br>
環境変数`SDL_VIDEO_X11_NET_WM_BYPASS_COMPOSITOR`が設定されている場合、このプロパティは効果がない。
```csharp
public bool BypassCompositor { get; set; } = true;
```
### Type
|Name|Description|
|:-|:-|
|bool||