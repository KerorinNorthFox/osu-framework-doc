- [Class HostOptions #](#class-hostoptions-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Properties](#properties)
    - [BindIPC](#bindipc)
      - [Declaration](#declaration)
      - [Type](#type)
    - [PortableInstallation](#portableinstallation)
      - [Declaration](#declaration-1)
      - [Type](#type-1)
    - [BypassCompositor](#bypasscompositor)
      - [Declaration](#declaration-2)
      - [Type](#type-2)


# Class HostOptions [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/HostOptions.cs#L11)
[Host]()のさまざまな構成プロパティ。


## Namespace
osu.Framework


## Syntax
```csharp
public class HostOptions
```


## Properties

### BindIPC
IPC ポートをバインドするかどうか。使用法の詳細については、[IIpcHost]()を参照。
#### Declaration
```csharp
public bool BindIPC { get; set; }
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### PortableInstallation
これがポータブルインストールであるかどうか。すべてのゲーム ファイルは、標準のデータディレクトリではなく、実行可能ファイルと一緒に配置される。
#### Declaration
```csharp
public bool PortableInstallation { get; set; }
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### BypassCompositor
コンポジターをバイパスするかどうか。デフォルトは`true`。<br>
Linux では、コンポジターはさまざまなウィンドウ効果を適用するためにアプリケーションを再バッファリングするため、プロセスのレイテンシーが増加する。したがって、ゲームではこれをバイパスするのが得策だが、普通のアプリケーションでは通常、ウィンドウの効果をそのままにしておく方が有益である。<br>
環境変数`SDL_VIDEO_X11_NET_WM_BYPASS_COMPOSITOR`が設定されている場合、このプロパティは効果がない。
#### Declaration
```csharp
public bool BypassCompositor { get; set; } = true;
```
#### Type
|Name|Description|
|:-|:-|
|bool||