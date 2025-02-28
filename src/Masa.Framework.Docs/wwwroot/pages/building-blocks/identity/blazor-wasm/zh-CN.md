## 概念

用于`Blazor WebAssembly`项目, 提供的用户身份信息来源于`AuthenticationStateProvider`

## 使用

1. 安装`Masa.Contrib.Authentication.Identity.BlazorWebAssembly`

```csharp
dotnet add package Masa.Contrib.Authentication.Identity.BlazorWebAssembly
```

2. 注册`MasaIdentity`, 修改`Program.cs`

```csharp
builder.Services.AddMasaIdentity();
```

3. 获取用户信息

```csharp
IUserContext userContext;//从DI获取
var userId = userContext.GetUserId<Guid>();
```