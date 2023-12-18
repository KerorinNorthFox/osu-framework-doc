- [Class FileCallbacks #](#class-filecallbacks-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
  - [Properties](#properties)
    - [Callbacks](#callbacks)
      - [Declaration](#declaration-2)
      - [Type](#type)
  - [Methods](#methods)
    - [Length](#length)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-2)
      - [Return](#return)
    - [Seek](#seek)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-3)
      - [Return](#return-1)
    - [Read](#read)
      - [Declaration](#declaration-5)
      - [Arguments](#arguments-4)
    - [Close](#close)
      - [Declaration](#declaration-6)
      - [Arguments](#arguments-5)



# Class FileCallbacks [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/FileCallbacks.cs#L18)
[FileProcedures]()のラッパーで、[BassCallback]()の機能を提供する。<br>
[IFileProcedures]()インターフェイスを実装するクラスに委任できる。


## Namespace
osu.Framework.Audio.Callbacks


## Implements
[BassCallback]()


## Syntax
```csharp
public class FileCallbacks : BassCallback
```


## Constructor
#### Declaration
```csharp
public FileCallbacks(IFileProcedures implementation)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`implementation`|[IFileProcedures]()||

---
#### Declaration
```csharp
public FileCallbacks(FileProcedures procedures)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`procedures`|[FileProcedures]()||


## Properties

### Callbacks
#### Declaration
```csharp
public FileProcedures Callbacks { get; private set; }
```
#### Type
|Type|Description|
|:-|:-|
|[FileProcedures]()||


## Methods

### Length
#### Declaration
```csharp
public long Length(IntPtr user) => implementation?.Length(user) ?? procedures.Length(user);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`user`|[IntPtr]()||
#### Return
|Type|Description|
|:-|:-|
|long||

### Seek
#### Declaration
```csharp
public bool Seek(long offset, IntPtr user) => implementation?.Seek(offset, user) ?? procedures.Seek(offset, user);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`offset`|long||
|`user`|[IntPtr]()||
#### Return
|Type|Description|
|:-|:-|
|bool||

### Read
#### Declaration
```csharp
public int Read(IntPtr buffer, int length, IntPtr user) => implementation?.Read(buffer, length, user) ?? procedures.Read(buffer, length, user);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`buffer`|[IntPtr]()||
|`length`|int||
|`user`|[IntPtr]()||

### Close
#### Declaration
```csharp
public void Close(IntPtr user)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`user`|[IntPtr]()||