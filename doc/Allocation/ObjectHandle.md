- [Struct ObjectHandle\<T\> #](#struct-objecthandlet-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)
  - [Fields](#fields)
    - [Handle](#handle)
      - [Declaration](#declaration-2)
      - [Type](#type)
    - [Address](#address)
      - [Declaration](#declaration-3)
      - [Type](#type-1)
    - [IsAllocated](#isallocated)
      - [Declaration](#declaration-4)
      - [Type](#type-2)
  - [Methods](#methods)
    - [](#)



# Struct ObjectHandle\<T\> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ObjectHandle.cs#L14)
[IDisposable]()パターンをサポートする[GCHandle]()のラッパー。


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()


## Syntax
```csharp
public struct ObjectHandle<T> : IDisposable
    where T : class
```


## Constructor
指定された[GCHandleType]()を使用して、指定されたオブジェクトを[GCHandle]()でラップする。
#### Declaration
```csharp
public ObjectHandle(T target, GCHandleType handleType)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`target`|T|ラップするターゲットオブジェクト。|
|`handleType`|[GCHandleType]()|使用するハンドルの型。|

---
渡された[IntPtr]()に基づいて[ObjectHandle\<T\>]()を再作成する。<br>
このオブジェクトを破棄してもハンドルは解放されず、代わりに元のオブジェクトを破棄する必要がある。
#### Declaration
```csharp
public ObjectHandle(IntPtr handle)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`handle`|[IntPtr]()|ハンドル|


## Fields

### Handle
[GCHandle]()からのポインター (割り当てられている場合)。それ以外の場合は、[IntPtr.Zero]()を参照。
#### Declaration
```csharp
public IntPtr Handle => handle.IsAllocated ? GCHandle.ToIntPtr(handle) : IntPtr.Zero;
```
#### Type
|Type|Description|
|:-|:-|
|[IntPtr]()||

### Address
ターゲット オブジェクトが割り当てられ固定されている場合はそのアドレス。それ以外の場合は、[IntPtr.Zero]()を参照。<br>
注: これは[Handle]()とは異なる。
#### Declaration
```csharp
public IntPtr Address => handle.IsAllocated ? handle.AddrOfPinnedObject() : IntPtr.Zero;
```
#### Type
|Type|Description|
|:-|:-|
|[IntPtr]()||

### IsAllocated
#### Declaration
```csharp
public bool IsAllocated => handle.IsAllocated;
```
#### Type
|Type|Description|
|:-|:-|
|bool||


## Methods

### 