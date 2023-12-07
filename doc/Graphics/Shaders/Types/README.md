# osu.Framework.Graphics.Shaders.Types Doc
- [osu.Framework.Graphics.Shaders.Types Doc](#osuframeworkgraphicsshaderstypes-doc)
- [構造体](#構造体)
  - [`UniformBool` #](#uniformbool-)
  - [`UniformFloat` #](#uniformfloat-)
  - [`UniformInt` #](#uniformint-)
  - [`UniformMatrix3` #](#uniformmatrix3-)
  - [`UniformMatrix4` #](#uniformmatrix4-)
  - [`UniformPadding12` #](#uniformpadding12-)
  - [`UniformPadding4` #](#uniformpadding4-)
  - [`UniformPadding8` #](#uniformpadding8-)
  - [`UniformVector2` #](#uniformvector2-)
  - [`UniformVector3` #](#uniformvector3-)
  - [`UniformVector4` #](#uniformvector4-)

# 構造体
## `UniformBool` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformBool.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 4)]
public record struct UniformBool
```

## `UniformFloat` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformFloat.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 4)]
public record struct UniformFloat
```

## `UniformInt` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformInt.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 4)]
public record struct UniformInt
```

## `UniformMatrix3` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformMatrix3.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 48)]
public record struct UniformMatrix3
```

## `UniformMatrix4` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformMatrix4.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 64)]
public record struct UniformMatrix4
```

## `UniformPadding12` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformPadding12.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential, Size = 12)]
public record struct UniformPadding12;
```

## `UniformPadding4` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformPadding4.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential, Size = 4)]
public record struct UniformPadding4;
```

## `UniformPadding8` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformPadding8.cs#L12)
```csharp
[StructLayout(LayoutKind.Sequential, Size = 8)]
public record struct UniformPadding8;
```

## `UniformVector2` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformVector2.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 8)]
public record struct UniformVector2
```

## `UniformVector3` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformVector3.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 16)]
public record struct UniformVector3
```

## `UniformVector4` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Types/UniformVector4.cs#L13)
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 1, Size = 16)]
public record struct UniformVector4
```