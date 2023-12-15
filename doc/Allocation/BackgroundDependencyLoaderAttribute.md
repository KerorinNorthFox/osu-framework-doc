- [Class BackgroundDependencyLoaderAttribute #](#class-backgrounddependencyloaderattribute-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments)


# Class BackgroundDependencyLoaderAttribute [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/BackgroundDependencyLoaderAttribute.cs#L23)
メソッドを[Graphics.Drawable]()の (非同期の可能性がある) 初期化メソッドとしてマークし、メソッドのパラメーターを介して依存関係を自動的に挿入できるようにする。


## Namespace
osu.Framework.Allocation


## Implements
[Attribute]()


## Syntax
```csharp
[MeansImplicitUse(ImplicitUseKindFlags.InstantiatedNoFixedConstructorSignature)]
[AttributeUsage(AttributeTargets.Method)]
public class BackgroundDependencyLoaderAttribute : Attribute
```


## Constructor
依存関係注入のコンテキストで、このメソッドをクラスの (非同期の可能性がある) イニシャライザとしてマークする。
#### Declaration
```csharp
public BackgroundDependencyLoaderAttribute()
```
---
依存関係注入のコンテキストで、このメソッドをクラスの (非同期の可能性がある) イニシャライザとしてマークする。
#### Declaration
```csharp
public BackgroundDependencyLoaderAttribute(bool permitNulls)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`permitNulls`|bool||