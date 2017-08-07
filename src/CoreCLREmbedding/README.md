# .Net Core CLR

## Documentation

Usage: [../../README.md#using-net-core](../../README.md#using-net-core)

Opening issue: https://github.com/tjanczuk/edge/issues/279
Current implementation issue: https://github.com/tjanczuk/edge/issues/433

Hosting .Net Core: https://docs.microsoft.com/en-us/dotnet/core/tutorials/netcore-hosting

## Why so many files?

.Net Core hosting needs that all assemblies (Framework and external libraries) are harvested before initialization.
This work must be done in a cross-platform way.
Most files in sub directories are copied from https://github.com/dotnet/core-setup/tree/master/src/corehost/cli (v1.0.x), although the structure isn't identical and some files have minor tweaks.

## Edge.Js requirement

This library is required when using Node from C#. But it's also required when using `.Net Core` from Node.
Once `.Net Core` is initialized, some helper methods are binded to Edge.Js library in order to provide functionality that is implemented in .Net land:
- Compile embedded C# code from Node.
- Marshall data from C# to Node using an intermediate representation (defined in edge.h).
