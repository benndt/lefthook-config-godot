# Godot Lefthook Configurations

This repository provides [lefthook](https://github.com/evilmartians/lefthook) configurations for Godot projects.

## Usage

Add the following to your `.lefthook.yaml`:

```yaml
remotes:
  - git_url: https://github.com/benndt/lefthook-config-godot
    refetch_frequency: 24h
    configs:
      - gdtoolkit.yaml
```

### gdtoolkit

Once you have installed [gdtoolkit](https://github.com/Scony/godot-gdscript-toolkit), you can either add the configuration for all gdtoolkit tools:

```yaml
remotes:
  # …
    configs:
      - gdtoolkit.yaml
```

or add individual ones:

```yaml
remotes:
  # …
    configs:
      - gdtoolkit/gdformat.yaml
      - gdtoolkit/gdlint.yaml
      - gdtoolkit/gdradon.yaml
```

#### Configs

To change the default error levels for gdradon you can define a lefthook template inside your `.lefthook.yaml`:

```yaml
templates:
  gdradon_error_levels: B|C|D|E|F
```
