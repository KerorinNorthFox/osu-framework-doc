- [Struct ValueInvokeOnDisposal #](#struct-valueinvokeondisposal-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Methods](#methods)
    - [Dispose](#dispose)
      - [Declaration](#declaration-1)
- [Struct ValueInvokeOnDisposal\<T\> #](#struct-valueinvokeondisposalt-)
  - [Namespace](#namespace-1)
  - [Implements](#implements-1)
  - [Syntax](#syntax-1)
  - [Constructor](#constructor-1)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-1)
  - [Methods](#methods-1)
    - [Dispose](#dispose-1)
      - [Declaration](#declaration-3)



# Struct ValueInvokeOnDisposal [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ValueInvokeOnDisposal.cs#L18)
この構造体のインスタンスは、後でクリーンアップするためのアクションをキャプチャする。適切な使用法は次のとおりである：
```csharp
using (SomeMethod())
{
    // ...
}
```
using ブロックは、返されたインスタンスを自動的に破棄し、必要なクリーンアップ作業を実行する。<br>
これは、割り当てを最小限に抑える必要がある場合に使用される[InvokeOnDisposal]()の構造体バージョン。


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()


## Syntax
```csharp
public readonly struct ValueInvokeOnDisposal : IDisposable
```


## Constructor
新しいインスタンスを構築し、破棄中に実行される指定されたアクションをキャプチャする。
#### Declaration
```csharp
public ValueInvokeOnDisposal(Action action)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`action`|[Action]()|廃棄中に呼び出すアクション。|


## Methods

### Dispose
このインスタンスを破棄し、最初にキャプチャされたアクションを呼び出す。
#### Declaration
```csharp
public void Dispose()
```



---
# Struct ValueInvokeOnDisposal\<T\> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ValueInvokeOnDisposal.cs#L55)
この構造体のインスタンスは、後でクリーンアップするためのアクションをキャプチャする。適切な使用法は次のとおりである：
```csharp
using (SomeMethod())
{
    // ...
}
```
using ブロックは、返されたインスタンスを自動的に破棄し、必要なクリーンアップ作業を実行する。<br>
これは、割り当てを最小限に抑える必要がある場合に使用される[InvokeOnDisposal]()の構造体バージョン。


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()


## Syntax
```csharp
public readonly struct ValueInvokeOnDisposal<T> : IDisposable
```


## Constructor
新しいインスタンスを構築し、破棄中に実行される指定されたアクションをキャプチャする。
#### Declaration
```csharp
public ValueInvokeOnDisposal(T sender, Action<T> action)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`sender`|T|`action`コールバックに表示されるセンダー。|
|`action`|[Action]()\<T\>|廃棄中に呼び出すアクション。|


## Methods

### Dispose
このインスタンスを破棄し、最初にキャプチャされたアクションを呼び出す。
#### Declaration
```csharp
public void Dispose()
```