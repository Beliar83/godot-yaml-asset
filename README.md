# godot-yaml-asset
Godot yaml adds printing and parsing yaml data.

It uses yaml-cpp for the basic parsing and specific converters for Godot classes.

Supported classes are printed as either their matching yaml type or, if special handling is necessary, using a yaml tag to identify them as that special type.

Currently it prints and parses all Variant variables except objects and thus currently has the same behaviour as JSON.

Usage:

Since this is a godot native plugin, you first need to (pre)load it like this:

```
yaml = preload("res://addons/godot-yaml/gdyaml.gdns").new()
```

After this the basic usage is like for JSON:

To convert a value to a yaml string you need to use the print method, like this:

```
var yamlstring = yaml.print(1.0)
```

The parse method takes a yaml formatted string and tries to convert it into a godot variable

```
var value = yaml.parse(yamlstring)
```

If it cannot convert the string it will give an error message with information why it could not convert something and the position inside the string where it failed.
