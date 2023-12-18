- [Interface ISourceGeneratedDependencyActivator #](#interface-isourcegenerateddependencyactivator-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Methods](#methods)
    - [RegisterForDependencyActivation](#registerfordependencyactivation)
      - [Declaration](#declaration)
      - [Arguments](#arguments)



# Interface ISourceGeneratedDependencyActivator [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/ISourceGeneratedDependencyActivator.cs#L12)
依存関係をオブジェクトに注入するためにソース ジェネレーターによって実装される。<br>
このインターフェイスを手動で実装してはいけない。


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public interface ISourceGeneratedDependencyActivator
```


## Methods

### RegisterForDependencyActivation
このオブジェクトの依存関係アクティブ化関数を登録するために呼び出される。
#### Declaration
```csharp
void RegisterForDependencyActivation(IDependencyActivatorRegistry registry);
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`registry`|[IDependencyActivatorRegistry]()|`registry`アクティベーション機能を登録するための[IDependencyActivatorRegistry]()|