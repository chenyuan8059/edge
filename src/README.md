# Edge

Here are the sources for edge module.

* Node binary module in it's different flavors:
   * _dotnet_ - Windows full .Net environment
   * _mono_ - Mono for Linux/Mac
   * CoreCLR - .Net Core

* `Edge.Js` .Net module (under double/ directory)

## How to open projects in Visual Studio

### Node binary module

The project are configured with node-gyp.

In the root of the repo, use `node-gyp configure`, that will create the `build/binding.sln` with the three projects for the different flavors of the binary node module.
When built the output will be `edge.node` binary module.

### Edge.Js Nuget library

Open project double\Edge.js\Edge.js.xproj
This library required when using Node from .Net. It's also required for compiling C# code on-the-fly from edge when using .Net Core.
