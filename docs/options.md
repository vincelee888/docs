# List of options

### Autocomplete Service Runtime

The Ionide plugin relies on the F# compiler services for processing code in the editor.  The compiler services can run under the full framework (requiring `mono` on non-Windows platforms) or they can run under .NET Core as of Ionide 3.13.0.  This experimental feature can be enabled in the user settings.

`Preferences > Settings` and add a new setting 
```json
"FSharp.fsacRuntime": "netcore"
```

There are two options:

* `net` (default) full framework
* `netcore` .NET Core framework

After updating this setting, execute the "Reload Window" command in VS Code for the setting to take effect.

NOTE: projects that use functionality incompatible with .NET Core, such as type providers, require this be set to `net` in order for the F# Autocomplete Service to process code using these features.
