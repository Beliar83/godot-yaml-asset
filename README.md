# godot-yaml-asset
Godot yaml adds printing and parsing yaml data.

It uses yaml-cpp for the basic parsing and specific converters for Godot classes.

Supported classes are printed as either their matching yaml type or, if special handling is necessary, using a yaml tag to identify them as that special type.

Currently it prints and parses all Variant variables except objects and thus currently has the same behaviour as JSON.
