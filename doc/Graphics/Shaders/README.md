# osu.Framework.Graphics.Shaders Doc
- [osu.Framework.Graphics.Shaders Doc](#osuframeworkgraphicsshaders-doc)
- [インターフェース](#インターフェース)
  - [`IShader` #](#ishader-)
  - [`IShaderStore` #](#ishaderstore-)
  - [`IUniform` #](#iuniform-)
  - [`IUniformWithValue<T>` #](#iuniformwithvaluet-)
- [クラス](#クラス)
  - [`ComputeProgramCompilation` #](#computeprogramcompilation-)
  - [`ShaderCompilationStore` #](#shadercompilationstore-)
  - [`ShaderManager` #](#shadermanager-)
  - [`VertexShaderDescriptor` #](#vertexshaderdescriptor-)
  - [`FragmentShaderDescriptor` #](#fragmentshaderdescriptor-)
  - [`Uniform<T>` #](#uniformt-)
  - [`VertexFragmentShaderCompilation` #](#vertexfragmentshadercompilation-)
- [列挙型](#列挙型)
  - [`ShaderPartType` #](#shaderparttype-)

# インターフェース
## `IShader` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/IShader.cs#L10)
```csharp
public interface IShader : IDisposable
```

## `IShaderStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/IShaderStore.cs#L6)
```csharp
public interface IShaderStore
```

## `IUniform` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/IUniform.cs#L9)
```csharp
public interface IUniform
```

## `IUniformWithValue<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/IUniformWithValue.cs#L8)
```csharp
public interface IUniformWithValue<T> : IUniform
    where T : unmanaged, IEquatable<T>
```

# クラス
## `ComputeProgramCompilation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/ComputeProgramCompilation.cs#L8)
```csharp
public class ComputeProgramCompilation
```

## `ShaderCompilationStore` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/ShaderCompilationStore.cs#L16)
```csharp
public class ShaderCompilationStore
```

## `ShaderManager` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/ShaderManager.cs#L12)
```csharp
public class ShaderManager : IShaderStore, IDisposable
```

## `VertexShaderDescriptor` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/ShaderManager.cs#L149)
```csharp
public static class VertexShaderDescriptor
```

## `FragmentShaderDescriptor` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/ShaderManager.cs#L156)
```csharp
public static class FragmentShaderDescriptor
```

## `Uniform<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/Uniform.cs#L9)
```csharp
public class Uniform<T> : IUniformWithValue<T>
    where T : unmanaged, IEquatable<T>
```

## `VertexFragmentShaderCompilation` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/VertexFragmentShaderCompilation.cs#L8)
```csharp
public class VertexFragmentShaderCompilation
```

# 列挙型
## `ShaderPartType` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/Shaders/ShaderPartType.cs#L6)
```csharp
public enum ShaderPartType
```