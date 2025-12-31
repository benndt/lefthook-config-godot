# lefthook-config-godot

## Requirements

- [lefthook](https://github.com/evilmartians/lefthook)
- [gdtoolkit](https://github.com/Scony/godot-gdscript-toolkit)

## Usage

Add the following to your `.lefthook.yaml`:

```yaml
remotes:
  - git_url: https://github.com/benndt/lefthook-config-godot
    refetch_frequency: 24h
    configs:
      - gdtoolkit.yaml
```

### Custom error levels

To change the default error levels for gdradon you can define a lefthook template inside your `.lefthook.yaml`:

```yaml
templates:
  gdradon_error_levels: B|C|D|E|F
```
