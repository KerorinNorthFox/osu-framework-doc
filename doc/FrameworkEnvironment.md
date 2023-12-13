- [Property](#property)
  - [FrameworkEnvironment.StartupExecutionMode](#frameworkenvironmentstartupexecutionmode)
    - [Type](#type)
  - [FrameworkEnvironment.NoTestTimeout](#frameworkenvironmentnotesttimeout)
    - [Type](#type-1)
  - [FrameworkEnvironment.ForceTestGC](#frameworkenvironmentforcetestgc)
    - [Type](#type-2)
  - [FrameworkEnvironment.FrameStatisticsViaTouch](#frameworkenvironmentframestatisticsviatouch)
    - [Type](#type-3)
  - [FrameworkEnvironment.PreferredGraphicsSurface](#frameworkenvironmentpreferredgraphicssurface)
    - [Type](#type-4)
  - [FrameworkEnvironment.PreferredGraphicsRenderer](#frameworkenvironmentpreferredgraphicsrenderer)
    - [Type](#type-5)
  - [FrameworkEnvironment.StagingBufferType](#frameworkenvironmentstagingbuffertype)
    - [Type](#type-6)
  - [FrameworkEnvironment.VertexBufferCount](#frameworkenvironmentvertexbuffercount)
    - [Type](#type-7)
  - [FrameworkEnvironment.NoStructuredBuffers](#frameworkenvironmentnostructuredbuffers)
    - [Type](#type-8)

# Property
## FrameworkEnvironment[.StartupExecutionMode](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L11)
```csharp
public static ExecutionMode? StartupExecutionMode { get; }
```
### Type
|Name|Description|
|:-|:-|
|[ExecutionMode?](./Platform/README.md#executionmode)|シングルスレッドかマルチスレッドか|

## FrameworkEnvironment[.NoTestTimeout](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L12)
```csharp
public static bool NoTestTimeout { get; }
```
### Type
|Name|Description|
|:-|:-|
|bool||

## FrameworkEnvironment[.ForceTestGC](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L13)
```csharp
public static bool ForceTestGC { get; }
```
### Type
|Name|Description|
|:-|:-|
|bool||

## FrameworkEnvironment[.FrameStatisticsViaTouch](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L14)
```csharp
public static bool FrameStatisticsViaTouch { get; }
```
### Type
|Name|Description|
|:-|:-|
|bool||

## FrameworkEnvironment[.PreferredGraphicsSurface](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L15)
```csharp
public static GraphicsSurfaceType? PreferredGraphicsSurface { get; }
```
### Type
|Name|Description|
|:-|:-|
|[GraphicsSurfaceType?](./Platform/README.md#graphicssurfacetype)|[IWindow](./Platform/README.md#iwindow)のグラフィックサーフェス。|

## FrameworkEnvironment[.PreferredGraphicsRenderer](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L16)
```csharp
public static string? PreferredGraphicsRenderer { get; }
```
### Type
|Name|Description|
|:-|:-|
|string?||

## FrameworkEnvironment[.StagingBufferType](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L17)
```csharp
public static int? StagingBufferType { get; }
```
### Type
|Name|Description|
|:-|:-|
|int?||

## FrameworkEnvironment[.VertexBufferCount](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L18)
```csharp
public static int? VertexBufferCount { get; }
```
### Type
|Name|Description|
|:-|:-|
|int?||

## FrameworkEnvironment[.NoStructuredBuffers](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L19)
```csharp
public static bool NoStructuredBuffers { get; }
```
### Type
|Name|Description|
|:-|:-|
|bool||