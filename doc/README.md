# osu.Framework Doc
- [osu.Framework Doc](#osuframework-doc)
- [Interface](#interface)
  - [`IStateful<T>` #](#istatefult-)
    - [Where](#where)
    - [Event](#event)
    - [Property](#property)
  - [`IUpdateable` #](#iupdateable-)
    - [Method](#method)
- [Class](#class)
  - [`FrameworkEnvironment` #](#frameworkenvironment-)
    - [Property](#property-1)
    - [Constructor](#constructor)
  - [`Game` #](#game-)
    - [Inherit](#inherit)
    - [Property](#property-2)
    - [Method](#method-1)
  - [`Host` #](#host-)
    - [Method](#method-2)
  - [`HostOptions` #](#hostoptions-)
    - [Property](#property-3)
  - [`RuntimeInfo` #](#runtimeinfo-)

# Interface
## `IStateful<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IStateful.cs#L12)
状態を持ち、外部コンシューマが現在の状態を変更できるようにするオブジェクト。
```csharp
public interface IStateful<T>
    where T : struct
```
### Where
|Type|Description|
|:-|:-|
|T|通常、このインターフェイスを実装するクラスに対してローカルな列挙型。|
### Event
|Name|Type|Access|
|:-|:-|:-|
|[StateChanged]()|Action\<T\>||
### Property
|Name|Type|Access|
|:-|:-|:-|
|[State]()|T||

## `IUpdateable` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/IUpdateable.cs#L6)
```csharp
public interface IUpdateable
```
### Method
|Name|Type|Access|
|:-|:-|:-|
|[Update]()|void||

# Class
## `FrameworkEnvironment` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L9)
```csharp
public static class FrameworkEnvironment
```
### Property
|Name|Type|Access|
|:-|:-|:-|
|[StartupExecutionMode](./FrameworkEnvironment.md#frameworkenvironmentstartupexecutionmode)|ExecutionMode?|static get|
|[NoTestTimeout](./FrameworkEnvironment.md#frameworkenvironmentnotesttimeout)|bool|static get|
|[ForceTestGC](./FrameworkEnvironment.md#frameworkenvironmentforcetestgc)|bool|static get|
|[FrameStatisticsViaTouch](./FrameworkEnvironment.md#frameworkenvironmentframestatisticsviatouch)|bool|static get|
|[PreferredGraphicsSurface](./FrameworkEnvironment.md#frameworkenvironmentpreferredgraphicssurface)|GraphicsSurfaceType?|static get|
|[PreferredGraphicsRenderer](./FrameworkEnvironment.md#frameworkenvironmentpreferredgraphicsrenderer)|string?|static get|
|[StagingBufferType](./FrameworkEnvironment.md#frameworkenvironmentstagingbuffertype)|int?|static get|
|[VertexBufferCount](./FrameworkEnvironment.md#frameworkenvironmentvertexbuffercount)|int?|static get|
|[NoStructuredBuffers](./FrameworkEnvironment.md#frameworkenvironmentnostructuredbuffers)|bool|static get|
### Constructor
```csharp
static FrameworkEnvironment()
```

## `Game` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Game.cs#L31)
```csharp
public abstract partial class Game : Container, IKeyBindingHandler<FrameworkAction>, IKeyBindingHandler<PlatformAction>, IHandleGlobalKeyboardInput
```
### Inherit
|Name|Description|
|:-|:-|
|[Container]()||
|[IKeyBindingHandler\<FrameworkAction\>]()||
|[IKeyBindingHandler\<PlatformAction\>]()||
|[IHandleGlobalKeyboardInput]()||
### Property
|Name|Type|Access|
|:-|:-|:-|
|[Window]()|IWindow|public|
|[Resources]()|ResourceStore<byte[]>|get; private set;|
|[Textures]()|TextureStore|get; private set;|
|[DefaultTextureFilteringMode]()|TextureFilteringMode|protected virtual|
|[Host]()|GameHost|protected|
|[IsActive]()|IBindable<bool>|public|
|[Audio]()|AudioManager|get; private set;|
|[Shaders]()|ShaderManager|get; private set;|
|[Fonts]()|FontStore|get; private set;|
|[Localisation]()|LocalisationManager|protected get; private set;|
|[Content]()|Container\<Drawable\>|protected|
|[FrameStatistics]()|Bindable\<FrameStatisticsMode\>|protected readonly|
### Method
|Name|Return|Access|
|:-|:-|:-|
|[CreateLocalisationManager]()|LocalisationManager|protected virtual|
|[CreateUserInputManager]()|UserInputManager|protected internal virtual|
|[GetFrameworkConfigDefaults]()|IDictionary<FrameworkSetting, object>|protected internal virtual|
|[CreateStorage]()|Storage|protected internal virtual|
|[SetHost]()|void|virtual|
|[CreateChildDependencies]()|IReadOnlyDependencyContainer|protected|
|[AddFont]()|void|public|
|[LoadComplete]()|void|protected|
|[OnPressed]()|bool|public|
|[CycleFrameStatistics]()|void|protected|
|[OnReleased]()|bool|public|
|[OnPressed]()|bool|virtual|
|[OnReleased]()|void|virtual|
|[RequestExit]()|void|public|
|[Exit]()|void|public|
|[OnExiting]()|bool|protected virtual|
|[Dispose]()|void|protected|

## `Host` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Host.cs#L15)
```csharp
public static class Host
```
### Method
|Name|Return|Access|
|:-|:-|:-|
|[GetSuitableDesktopHost]()|DesktopGameHost|static|

## `HostOptions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/HostOptions.cs#L11)
[Host]()のさまざまな構成プロパティ。
```csharp
public class HostOptions
```
### Property
|Name|Type|Access|
|:-|:-|:-|
|[BindIPC]()|bool|public|
|[PortableInstallation]()|bool|public|
|[BypassCompositor]()|bool|public|

## `RuntimeInfo` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/RuntimeInfo.cs#L10)
```csharp
public static class RuntimeInfo
```