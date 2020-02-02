# ErrorProne.Unity

**NOTE that it's just an idea, there's no code yet:** Visual Studion extension that contains Roslyn analyzers that prevent hard to debug mistypes that are specific to using Unity game engine.

## EPU001: Using Quaternion fields directly

Example:
```
// We're interested only in rotation relative to the ground:
var rotation = transform.rotation.y;
```

Most likely the intention was:
```
// We're interested only in rotation relative to the ground:
var rotation = transform.rotation.eulerAngles.y;
```

## Not planned

Magic method name mistype: While it's an example that easily comes to mind first, nowadays it's hard to mistype a magic method name anyway, thanks to IntelliSence provided by the *Tools for Unity* extension.
