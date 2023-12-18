- [Class BassCallback #](#class-basscallback-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
  - [Destructor](#destructor)
      - [Declaration](#declaration-1)
  - [Properties](#properties)
    - [Handle](#handle)
      - [Declaration](#declaration-2)
      - [Type](#type)
  - [Methods](#methods)
    - [Dispose](#dispose)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments)
    - [Dispose](#dispose-1)
      - [Declaration](#declaration-4)



# Class BassCallback [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/BassCallback.cs#L15)
Bassライブラリへのコールバックに使用される、オプションの固定[ObjectHandle\<T\>]()を提供する抽象クラス。


## Namespace
osu.Framework.Audio.Callbacks


## Implements
[IDisposable]()


## Syntax
```csharp
public abstract class BassCallback : IDisposable
```


## Constructor
#### Declaration
```csharp
protected BassCallback()
```


## Destructor
#### Declaration
```csharp
~BassCallback()
```


## Properties

### Handle
コールバックハンドル、またはオブジェクトが固定されていない場合は[IntPtr.Zero]()を参照。
#### Declaration
```csharp
public IntPtr Handle => handle.Handle;
```
#### Type
|Type|Description|
|:-|:-|
|[IntPtr]()||


## Methods

### Dispose
#### Declaration
```csharp
protected virtual void Dispose(bool disposing)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`disposing`|bool||

###  Dispose
#### Declaration
```csharp
public void Dispose()
```