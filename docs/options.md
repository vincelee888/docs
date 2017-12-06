# List of options

## F# Plugin options

### `FSharp.fsacRuntime`

Choose the runtime of FsAutoComplete (FSAC). Require restart

Possible values:

* `net` - run FSAC using Full Framework (mono on non-Windows)

* `netcore` (*Experimental*) - run FSAC using .Net Core.

Default value: `net`

### `FSharp.workspaceMode`

Choose the workspace mode - way in which projects are detected in currently opened folder.

Possible values:

* `sln` - Tries to detecl `.sln` file in current workspace. If there are more than one `.sln` files user will be asked which one to use. If there is no `.sln` file in workspace service will fallback to `directory` mode. Search performed by FSAC using `FSharp.workspaceModePeekDeepLevel` setting.

* `directory` - Ionide loads all detected projects in the directory. Search performed by FSAC using `FSharp.workspaceModePeekDeepLevel` setting.

* `ionideSearch` - Ionide loads all detected projects in the directory. Search performed by Ionide - it was default mode pre-3.0.0 version.

Default value: `sln`

### `FSharp.workspaceModePeekDeepLevel`

Defines the depth level of directory hierarchy when searching for sln/projects

Possible values: `[0...99]`

Default value: `2`

### `FSharp.workspaceLoader`

Choose way the FSAC loads projects

Possible values:

* `projects` - loading projects is invoked by `project` request from Ionide. It's done synchronusly, one-by-one on the plugin startup. Using `ProjectCracker` for non-SDK projects, `dotnet-project-info` for SDK based projects.

* `workspaceLoad` (*Experimental*) - loading projects is triggered by `workspaceLoad` request from Ionide. Process is done asynchronusly, notifications are pushed by FSAC to Ionide through web sockets.

Default value: `projects`

## Paket Plugin options

## FAKE Plugin options