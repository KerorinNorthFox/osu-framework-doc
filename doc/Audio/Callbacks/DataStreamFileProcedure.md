- [Class DataStreamFileProcedures #](#class-datastreamfileprocedures-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Methods](#methods)
    - [Close](#close)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
    - [Length](#length)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-2)
    - [Read](#read)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-3)
      - [Return](#return)
    - [Seek](#seek)
      - [Declaration](#declaration-4)
      - [Arguments](#arguments-4)
      - [Return](#return-1)



# Class DataStreamFileProcedures [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/DataStreamFileProcedures.cs#L12)
[Stream]()からの読み取りをサポートする[IFileProcedures]()の実装。


## Namespace
osu.Framework.Audio.Callbacks


## Implements
[IFileProcedures]()


## Syntax
```csharp
public class DataStreamFileProcedures : IFileProcedures
```


## Constructor
#### Declaration
```csharp
public DataStreamFileProcedures(Stream data)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`data`|[Stream]()||


## Methods

### Close
#### Declaration
```csharp
public void Close(IntPtr user)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`user`|[IntPtr]()||

### Length
#### Declaration
```csharp
public long Length(IntPtr user)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`user`|[IntPtr]()||

### Read
#### Declaration
```csharp
public unsafe int Read(IntPtr buffer, int length, IntPtr user)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`buffer`|[IntPtr]()||
|`length`|int||
|`user`|[IntPtr]()||
#### Return
|Type|Description|
|:-|:-|
|int||

### Seek
#### Declaration
```csharp
public bool Seek(long offset, IntPtr user)
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