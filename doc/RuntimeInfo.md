- [Class RuntimeInfo #](#class-runtimeinfo-)
  - [Using](#using)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Constructor](#constructor)
      - [Declaration](#declaration)
  - [Properties](#properties)
    - [StartupDirectory](#startupdirectory)
      - [Declaration](#declaration-1)
      - [Type](#type)
    - [OS](#os)
      - [Declaration](#declaration-2)
      - [Type](#type-1)
    - [IsUnix](#isunix)
      - [Declaration](#declaration-3)
      - [Type](#type-2)
    - [IsDesktop](#isdesktop)
      - [Declaration](#declaration-4)
      - [Type](#type-3)
    - [IsMobile](#ismobile)
      - [Declaration](#declaration-5)
    - [Type](#type-4)
    - [IsApple](#isapple)
      - [Declaration](#declaration-6)
    - [Type](#type-5)
  - [Methods](#methods)
    - [GetFrameworkAssemblyPath](#getframeworkassemblypath)
      - [Declaration](#declaration-7)
      - [Return](#return)
  - [Enum](#enum)
    - [Platform](#platform)
      - [Declaration](#declaration-8)
      - [Fields](#fields)


# Class RuntimeInfo [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/RuntimeInfo.cs#L10)


## Using
System

## Namespace
osu.Framework


## Syntax
```csharp
public static class RuntimeInfo
```


## Constructor
#### Declaration
```csharp
static RuntimeInfo()
```


## Properties

### StartupDirectory
このゲームの起動ディレクトリへの絶対パス。
#### Declaration
```csharp
public static string StartupDirectory { get; } = AppContext.BaseDirectory;
```
#### Type
|Name|Description|
|:-|:-|
|string||

---
### OS
#### Declaration
```csharp
public static Platform OS { get; }
```
#### Type
|Name|Description|
|:-|:-|
|[Platform]()||

---
### IsUnix
#### Declaration
```csharp
public static bool IsUnix => OS != Platform.Windows;
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### IsDesktop
#### Declaration
```csharp
public static bool IsDesktop => OS == Platform.Linux || OS == Platform.macOS || OS == Platform.Windows;
```
#### Type
|Name|Description|
|:-|:-|
|bool||

---
### IsMobile
#### Declaration
```csharp
public static bool IsMobile => OS == Platform.iOS || OS == Platform.Android;
```
### Type
|Name|Description|
|:-|:-|
|bool||

---
### IsApple
#### Declaration
```csharp
public static bool IsApple => OS == Platform.iOS || OS == Platform.macOS;
```
### Type
|Name|Description|
|:-|:-|
|bool||


## Methods

### GetFrameworkAssemblyPath
osu.Framework.dllの絶対パスを返す。
#### Declaration
```csharp
public static string GetFrameworkAssemblyPath()
```
#### Return
|Type|Description|
|:-|:-|
|string||


## Enum

### Platform
#### Declaration
```csharp
public enum Platform
```
#### Fields
|Name|Description|
|:-|:-|
|Windows||
|Linux||
|macOS||
|iOS||
|Android||