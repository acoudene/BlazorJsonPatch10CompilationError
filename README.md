Here a simple Blazor example where client part just referencing JsonPatch assembly in .Net 10 and get compilation error.

In summary, if I use in Client WebAssembly:
`<PackageReference Include="Microsoft.AspNetCore.JsonPatch" Version="10.0.0" />`

Then I will get this error:
`1>C:\Program Files\dotnet\sdk\10.0.100\Sdks\Microsoft.NET.Sdk\targets\Microsoft.NET.Sdk.FrameworkReferenceResolution.targets(544,5): error NETSDK1082: There was no runtime pack for Microsoft.AspNetCore.App available for the specified RuntimeIdentifier 'browser-wasm'.`

But no error if I put this previous one: 
`<PackageReference Include="Microsoft.AspNetCore.JsonPatch" Version="9.0.11" />`

Link to issue: https://github.com/dotnet/aspnetcore/issues/64330#issuecomment-3552960743

