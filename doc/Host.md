- [Class Host #](#class-host-)
  - [Namespace](#namespace)
  - [Syntax](#syntax)
  - [Methods](#methods)
    - [GetSuitableDesktopHost](#getsuitabledesktophost)
      - [Declaration](#declaration)
      - [Arguments](#arguments)
      - [Return](#return)


# Class Host [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Host.cs#L15)


## Namespace
osu.Framework


## Syntax
```csharp
public static class Host
```

## Methods

### GetSuitableDesktopHost
#### Declaration
```csharp
public static DesktopGameHost GetSuitableDesktopHost(string gameName, HostOptions hostOptions = null)
```
#### Arguments
|Name|Type|Description|
|:-|:-|:-|
|`gameName`|string||
|`hostOptions` = null|[HostOptions]()||
#### Return
|Type|Description|
|:-|:-|
|[DesktopGameHost]()||