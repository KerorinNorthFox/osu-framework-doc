- [Class InvokeOnDisposal #](#class-invokeondisposal-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
  - [Methods](#methods)
    - [Dispose](#dispose)
      - [Declaration](#declaration-1)
- [Class InvokeOnDisposal\<T\> #](#class-invokeondisposalt-)
  - [Namespace](#namespace-1)
  - [Implements](#implements-1)
  - [Syntax](#syntax-1)
  - [Constructor](#constructor-1)
      - [Declaration](#declaration-2)
      - [Arguments](#arguments-1)
  - [Methods](#methods-1)
    - [Dispose](#dispose-1)
      - [Declaration](#declaration-3)



# Class InvokeOnDisposal [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/InvokeOnDisposal.cs#L16)
このクラスのインスタンスは、後のクリーンアップのためにアクションをキャプチャする。メソッドがこのクラスのインスタンスを返す場合、適切な使用法は次のとおりである。
```csharp
using (SomeMethod())
{
    // ...
}
```
usingブロックは、返されたインスタンスを自動的に破棄し、必要なクリーンアップ作業を実行する。


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()


## Syntax
```csharp
public class InvokeOnDisposal : IDisposable
```


## Constructor
新しいインスタンスを構築し、破棄中に実行される指定されたアクションをキャプチャする。
#### Declaration
```csharp
public InvokeOnDisposal(Action action)
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
public virtual void Dispose()
```



---
# Class InvokeOnDisposal\<T\> [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/InvokeOnDisposal.cs#L51)


## Namespace
osu.Framework.Allocation


## Implements
[IDisposable]()

## Syntax
```csharp
public class InvokeOnDisposal<T> : IDisposable
```


## Constructor
新しいインスタンスを構築し、破棄中に実行される指定されたアクションをキャプチャする。
#### Declaration
```csharp
public InvokeOnDisposal(T sender, Action<T> action)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`sender`|T|`action`コールバックに表示されるセンダー。|
|`action`|[Action\<T\>]()|廃棄中に呼び出すアクション。|


## Methods

### Dispose
このインスタンスを破棄し、最初にキャプチャされたアクションを呼び出す。
#### Declaration
```csharp
public virtual void Dispose()
```