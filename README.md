# BlankInEx <img src="https://i.imgur.com/nxsAFhq.png" height=64 align="left" /> <img src="https://i.imgur.com/8KS2qsZ.png" height="64" align="right" />

A .NET Framework 3.5 BepInEx project template, made for the modern, non-2007 era.

## Features

- C# `.gitignore` and `.gitattributes`
- Simple `.editorconfig`
- BepInEx NuGet references (including Unity)
- Partial C# 9 support
- Assembly, BepInEx, and Thunderstore versioning on build
- Thunderstore packaging on build
- Thunderstore packaging workflow for GitHub CI

## Usage

Clone or template this repository to produce a copy, then make the following changes:

- [ ] Insert your name in [the license](LICENSE), or replace it entirely. MIT is included because it is a simple, permissive license that is popular within the C# ecosystem.
- [ ] Rename the project, namespace, and solution
- [ ] Populate [the manifest](BlankInEx/manifest.json)
- [ ] Build the project once. Building generates the `BepInPlugin` attribute from the manifest data, which your IDE will complain about if not present.

After the initial setup, you can program like you would normally. Building will bake the current git version, pulled using [MinVer](https://github.com/adamralph/minver).

When you are ready to package for Thunderstore:

- [ ] If you have additional DLL files that need to be copied, edit the `csproj` file and add them to the `ZipThunderstore` task
- [ ] Replace [the icon](BlankInEx/thunderstore/src/icon.png) with your own (256x256)
- [ ] Replace this readme file with your own. It is also linked within the Thunderstore package.

If you do not replace the icon, your package will look like this and I will laugh at you:

![default icon](BlankInEx/thunderstore/src/icon.png)

Build the project with the `Release` configuration and a Thunderstore package will appear within `BlankInEx/thunderstore/out`.
