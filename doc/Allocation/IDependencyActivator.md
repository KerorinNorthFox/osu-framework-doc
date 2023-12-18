- [Interface IDependencyActivatorRegistry #](#interface-idependencyactivatorregistry-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Methods](#methods)
    - [IsRegistered](#isregistered)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Return](#return)
    - [Register](#register)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments-1)



# Interface IDependencyActivatorRegistry [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/IDependencyActivator.cs#L11)
依存関係アクティブ化関数を登録するためのオブジェクトのインターフェース。


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public interface IDependencyActivatorRegistry
```


## Methods

### IsRegistered
依存関係アクティブ化関数が指定されたタイプに対してすでに登録されているかどうか。
#### Declaration
```csharp
bool IsRegistered(Type type);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|型|
#### Return
|Type|Description|
|:-|:-|
|bool||

### Register
指定された型の依存関係アクティブ化関数を登録する。
#### Declaration
```csharp
void Register(Type type, InjectDependencyDelegate? injectDel, CacheDependencyDelegate? cacheDel);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|型|
|`injectDel`|[InjectDependencyDelegate]()|オブジェクトに依存関係を注入する関数。|
|`cacheDel`|[CacheDependencyDelegate]()|オブジェクトの依存関係をキャッシュする関数。|