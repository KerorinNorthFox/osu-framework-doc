- [Class FrameworkEnvironment #](#class-frameworkenvironment-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
  - [Properties](#properties)
    - [StartupExecutionMode](#startupexecutionmode)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [NoTestTimeout](#notesttimeout)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
    - [ForceTestGC](#forcetestgc)
      - [Declaration](#declaration-3)
      - [Type](#type-2)
    - [FrameStatisticsViaTouch](#framestatisticsviatouch)
      - [Declaration](#declaration-4)
      - [Type](#type-3)
    - [PreferredGraphicsSurface](#preferredgraphicssurface)
      - [Declaration](#declaration-5)
      - [Type](#type-4)
    - [PreferredGraphicsRenderer](#preferredgraphicsrenderer)
      - [Declaration](#declaration-6)
      - [Type](#type-5)
    - [StagingBufferType](#stagingbuffertype)
      - [Declaration](#declaration-7)
      - [Type](#type-6)
    - [VertexBufferCount](#vertexbuffercount)
      - [Declaration](#declaration-8)
      - [Type](#type-7)
    - [NoStructuredBuffers](#nostructuredbuffers)
      - [Declaration](#declaration-9)
      - [Type](#type-8)



# Class FrameworkEnvironment [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/FrameworkEnvironment.cs#L9)


## Namespace
osu.Framework


## Syntax
```csharp
public static class FrameworkEnvironment
```


## Constructor
#### Declaration
```csharp
static FrameworkEnvironment()
```


## Properties

### StartupExecutionMode
#### Declaration
```csharp
public static ExecutionMode? StartupExecutionMode { get; }
```
#### Type
|Name|Description|
|:-|:-|
|[ExecutionMode?]()|シングルスレッドかマルチスレッドか|

---
### NoTestTimeout
#### Declaration
```csharp
public static bool NoTestTimeout { get; }
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### ForceTestGC
#### Declaration
```csharp
public static bool ForceTestGC { get; }
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### FrameStatisticsViaTouch
#### Declaration
```csharp
public static bool FrameStatisticsViaTouch { get; }
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### PreferredGraphicsSurface
#### Declaration
```csharp
public static GraphicsSurfaceType? PreferredGraphicsSurface { get; }
```
#### Type
|Name|Description|
|:-|:-|
|[GraphicsSurfaceType?](./Platform/README.md#graphicssurfacetype)|[IWindow](./Platform/README.md#iwindow)のグラフィックサーフェス。|

---
### PreferredGraphicsRenderer
#### Declaration
```csharp
public static string? PreferredGraphicsRenderer { get; }
```
#### Type
|Name|Description|
|:-|:-|
|string?||

---
### StagingBufferType
#### Declaration
```csharp
public static int? StagingBufferType { get; }
```
#### Type
|Name|Description|
|:-|:-|
|int?||

---
### VertexBufferCount
#### Declaration
```csharp
public static int? VertexBufferCount { get; }
```
#### Type
|Name|Description|
|:-|:-|
|int?||

---
### NoStructuredBuffers
#### Declaration
```csharp
public static bool NoStructuredBuffers { get; }
```
#### Type
|Name|Description|
|:-|:-|
|bool||