# Nuget template
Template to create new nuget

## How to install

```bash
dotnet new -i RamosISW.Templates.NuGetLib.CSharp
```

If it was installed correctly you will see the following in your terminal.

```
Templates                           Short Name         Language          Tags
----------------------------------------------------------------------------------------
Console Application                 console            [C#], F#, VB      Common/Console
NuGet library                       nuget-lib          [C#]              Common/Library
Class library                       classlib           [C#], F#, VB      Common/Library
Unit Test Project                   mstest             [C#], F#, VB      Test/MSTest
NUnit 3 Test Project                nunit              [C#], F#, VB      Test/NUnit
NUnit 3 Test Item                   nunit-test         [C#], F#, VB      Test/NUnit
xUnit Test Project                  xunit              [C#], F#, VB      Test/xUnit
Razor Page                          page               [C#]              Web/ASP.NET
```

## How to use

```bash
dotnet new nuget-lib -n MyAwesomeNuget #You can change "myawesome" for the one you want
```
The above command will create a folder with the following structure

```
\---MyAwesomeNuget
        .gitignore
        Class1.cs
        LICENSE
        MyAwesomeNuget.csproj
        MyAwesomeNuget.nuspec.xml
```

If you compile the project, the file named `*.nuspec.xml` will change to `*.nuspec` automatically. And a package ready to be used will be produced in the path `$projectDir/publish/MyAwesomeNuget.1.0.0.nupkg`. This package can be used locally to ensure that it will work properly, you can use the following command to install it locally.
```bash
dotnet add package MyAwesomeNuget -s <Absolute_Path_To_Nupkg_File>
```
