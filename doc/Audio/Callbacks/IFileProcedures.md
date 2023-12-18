- [Interface IFileProcedures #](#interface-ifileprocedures-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Methods](#methods)
    - [Length](#length)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Return](#return)
    - [Close](#close)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
    - [Seek](#seek)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-2)
      - [Return](#return-1)
    - [Read](#read)
      - [Declaration](#declaration-3)
      - [Arguments](#arguments-3)
      - [Return](#return-2)



# Interface IFileProcedures [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Audio/Callbacks/IFileProcedures.cs#L12)
[FileProcedures]()構造体の定義と厳密に一致するインターフェース。


## Namespace
osu.Framework.Audio.Callbacks


## Syntax
```csharp
public interface IFileProcedures
```


## Methods

### Length
#### Declaration
```csharp
long Length(IntPtr user);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`user`|[IntPtr]()||
#### Return
|Type|Description|
|:-|:-|
|long||

### Close
#### Declaration
```csharp
void Close(IntPtr user);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`user`|[IntPtr]()||

### Seek
#### Declaration
```csharp
bool Seek(long offset, IntPtr user);
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
int Read(IntPtr buffer, int length, IntPtr user);
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