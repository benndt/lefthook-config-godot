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

Required tool: [gdtoolkit](https://github.com/Scony/godot-gdscript-toolkit).
You can either add the configuration for all gdtoolkit commands or add individual ones to your `remotes` config.

```yaml
configs:
  - gdtoolkit.yaml
  - gdtoolkit/gdformat.yaml
  - gdtoolkit/gdlint.yaml
  - gdtoolkit/gdradon.yaml
```

#### Customization

To change the error levels for gdradon you can define the following `templates` inside your `.lefthook.yaml`:

```yaml
templates:
  gdradon_error_levels: B|C|D|E|F
```

### Lizard

Required tool: [Lizard](https://github.com/terryyin/lizard)

```yaml
configs:
  - lizard.yaml
```

#### Customization

To change the Lizard command arguments you can define the following `templates` inside your `.lefthook.yaml`:

```yaml
templates:
  lizard_cyclomatic_complexity: 15
  lizard_length: 50
  lizard_nloc: 40
  lizard_parameter_count: 6
  lizard_working_threads: 10
  lizard_exclude: "src/addons/*"
```

### GdUnit4

Required tool: [gdUnit4](https://github.com/godot-gdunit-labs/gdUnit4)

```yaml
configs:
  - gdunit4.yaml
```

#### Customization

To change the GdUnit4 command arguments you can define the following `templates` inside your `.lefthook.yaml`:

```yaml
templates:
  godot_binary: "/path/to/godot"
  gdunit_test_folder: "tests"
  gdunit_report_folder: ".reports"
```
