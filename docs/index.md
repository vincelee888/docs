# Ionide

Ionide is a [Visual Studio Code](https://code.visualstudio.com/) package suite for cross platform F# development.

## Overview

Ionide for VSCode is set of 3 plugins avaliable in VSCode marketplace.

* [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) - provides F# specific features including advanced editor features (autocomplete, go-to definition, tooltips, rename, various refactorings and quick fix suggestions), integration with .Net project system, project explorer for project file visualization and manipulation, integration with MsBuild for building and running applications, debugger integration and more.

* [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) - provides integration with Paket - package dependency manager for .NET with support for NuGet packages and GitHub repositories.

* [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fake) - FAKE (F# Make) is popular F# tool and DSL for build orchestration.

## Requirements

* Visual Studio Code - it is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux created by Microsoft. For detailed documentation of editor, getting-started guides and more visit [official documentation](https://code.visualstudio.com/docs).

* F# - it is a mature, open source, cross-platform, functional-first programming language. It empowers users and organizations to tackle complex computing problems with simple, maintainable and robust code. Ionide supports any version of F# >= 3.0 but we do recommend using F# 4.1. Detailed installation instructions can be found of F# Software foundation webpage - for [Windows](http://fsharp.org/use/windows/), [MacOS](http://fsharp.org/use/mac/), and [Linux](http://fsharp.org/use/linux/)

* MsBuild 2015 (Windows only) - On Windows MsBuild 2015 (14.0) needs to be additionally installed. You can download it [here](https://www.microsoft.com/en-us/download/details.aspx?id=48159)

* .Net Core SDK (optional) - .Net Core is lightweight, cross platform, modern implementation of .Net Framework. We strongly recommend installing it since some advanced Ionide features such as debugging and project scaffolding depends on SDK and `dotnet` CLI tooling even if your application is targetting Full Framework. For detailed instructions on installing .Net Core visit [official step-by-step installation guide](https://www.microsoft.com/net/core)

## Plugin installation

Any VSCode extension can be installed using UI just inside VSCode. Bring up the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of VS Code or the `View: Extensions` command (`Ctrl+Shift+X`). Then in search box type `Ionide` to find all 3 extensions we provide. Click the `Install` button and after a successful install, you'll see an `Reload` button which will prompt you to restart VS Code to enable the new extension. For more detailed information about plugin installation visit [VSCode documentation](https://code.visualstudio.com/docs/editor/extension-gallery)

## Plugin activation

VSCode plugins are running in external processes (which means they should never impact editor performance) and are activated lazily, when certain activation events happens. This means that plugins are not loaded unnecesserly, for example when you don't work on project using given programming language.

Ionide plugins are activated when:

* Opened workspace contains any `.fsproj`, `.fs`, or `.fsx` file

* New `.fsproj`, `.fs`, or `.fsx` file is created in workspace that was not containing those files before.
