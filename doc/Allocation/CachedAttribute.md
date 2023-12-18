- [Class CachedAttribute #](#class-cachedattribute-)
  - [Namespace](#namespace)
  - [Implements](#implements)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
      - [Declaration](#declaration-1)
      - [Arguments](#arguments)
  - [Properties](#properties)
    - [Type](#type)
      - [例1](#例1)
      - [Declaration](#declaration-2)
      - [例2](#例2)
      - [Type](#type-1)
    - [Name](#name)
      - [Declaration](#declaration-3)
      - [Type](#type-2)
- [Class NullDependencyException #](#class-nulldependencyexception-)
  - [Namespace](#namespace-1)
  - [Syntax](#syntax-1)
  - [Constructor](#constructor-1)
      - [Declaration](#declaration-4)
      - [Type](#type-3)


# Class CachedAttribute [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/CachedAttribute.cs#L55)
[Drawable]()のクラス、インターフェイス、フィールド、またはプロパティ定義に添付して、値を依存関係としてキャッシュする必要があることを示す属性。<br>
キャッシュされた値は、[BackgroundDependencyLoaderAttribute]()または[ResolvedAttribute]()を通じて解決できる。<br>
この属性の動作は、それが配置されるメンバーのタイプに応じて意味が異なる。<br>
- フィールドとプロパティの場合、フィールドまたはプロパティを含むドローアブルの子の依存関係がキャッシュされる。
- [Type]()で別途指定しない限り、依存関係はフィールド/プロパティ値の具体的な (最も派生した) 型を使用してキャッシュされる。<br>詳細については、[Type]()プロパティのドキュメントの例のセクションを参照。
- [CachedAttribute]()の注釈が付けられたクラスのインスタンスは、それ自体の子のためにキャッシュされる。<br>[Type]()で別途指定しない限り、依存関係は [CachedAttribute]()が宣言された時点のタイプを使用してキャッシュされる。<br>[CachedAttribute]()自体は継承されないが、派生クラスのインスタンスは基本クラスを使用して自身をキャッシュすることに注意。<br>詳細については、[Type]()プロパティのドキュメントの例のセクションを参照。
- クラスが[CachedAttribute]()の注釈が付けられたインターフェイスを実装している場合、そのクラスのインスタンスは、そのインターフェイス型を使用して自身の子のために自分自身をキャッシュする。<br>クラスと同様、[CachedAttribute]()もインターフェイス間で継承されませんが、クラスのインスタンスは、実装するすべてのキャッシュ可能なインターフェイス タイプを使用して、それ自体を子にキャッシュする。


## Namespace
osu.Framework.Allocation


## Implements
[Attribute]()


## Syntax
```csharp
[MeansImplicitUse]
[AttributeUsage(AttributeTargets.Class | AttributeTargets.Field | AttributeTargets.Property | AttributeTargets.Interface, AllowMultiple = true, Inherited = false)]
public class CachedAttribute : Attribute
```


## Constructor
[DependencyContainer]()にキャッシュされるメンバーを識別する。
#### Declaration
```csharp
public CachedAttribute()
```
---
[DependencyContainer]()にキャッシュされるメンバーを識別する。
#### Declaration
```csharp
public CachedAttribute(Type type = null, string name = null)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`type`|[Type]()|メンバーをキャッシュする型。|
|`name`|string|キャッシュ内でメンバーを識別するための名前。|


## Properties

### Type
値をキャッシュする型。null の場合、型は属性が配置されるメンバーのタイプによって異なる。
- フィールドとプロパティの場合、属性はフィールド/プロパティの値の具体的/最も派生した型を使用する。
- クラスとインターフェイスの場合、属性は[CachedAttribute]()が直接配置されたクラス/インターフェイスタイプを使用する。
#### 例1
フィールドとプロパティのとき、この値が次のフィールド定義の`null`である場合:
```csharp
[Cached]
private BaseType obj = new DerivedType();
```
#### Declaration
```csharp
public Type Type;
```
そしてキャッシュされた型は`DerivedType`になる。
#### 例2
クラスの場合、次の構造があるとする。
```csharp
[Cached]
public class A { }

public class B : A { }
```
次のようなことが起こる。
- `A`のインスタンスは、型`A`を使用して自身を子にキャッシュする。
- `B`のインスタンスは、型`A`を使用して自身を子にキャッシュする。
- `B`のインスタンスは、型`B`を使用して子に自身をキャッシュしない。<br>
  この効果を実現するには、クラス`B`で[CachedAttribute]()を繰り返す必要がある。

インターフェイス継承階層に配置された[CachedAttribute]()は、クラスについて上で説明したルールと同様のルールに従う。
#### Type
|Type|Description|
|:-|:-|
|[Type]()||

---
### Name
このメンバーを識別するための名前。<br>
親を提供するカスタム[CacheInfo]()を使用してメンバーがキャッシュされている場合、名前はフィールド/プロパティから自動的に推測される。
#### Declaration
```csharp
public string Name;
```
#### Type
|Type|Description|
|:-|:-|
|string||


---
# Class NullDependencyException [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Allocation/CachedAttribute.cs#L218)
[CachedAttribute]()を使用して`null`をキャッシュしようとしたときに投げられる例外。


## Namespace
osu.Framework.Allocation


## Syntax
```csharp
public sealed class NullDependencyException : InvalidOperationException
```


## Constructor
#### Declaration
```csharp
public NullDependencyException(string message)
    : base(message)
```
#### Type
|Name|Type|Description|
|:-|:-|:-|
|`message`|string||