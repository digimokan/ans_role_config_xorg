# ans_role_config_xorg

Install the base, minimal Xorg display server.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_xorg.svg?label=release)](https://github.com/digimokan/ans_role_config_xorg/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Parent Role As Dependency](#use-from-parent-role-as-dependency)
* [Contributing](#contributing)

## Purpose

* Install base, minimal [Xorg](https://www.x.org/wiki/) display server.
* Do not install extra Xorg add-on fonts, apps, utilities, etc.

## Supported Operating Systems

* Arch Linux.
* FreeBSD.

## Quick Start

### Use From Parent Role As Dependency

1. List in parent role's `meta/requirements.yml`:

   ```yaml
   - src: https://github.com/digimokan/ans_role_config_xorg
   ```

2. Invoke explicitly in a task in parent role:

   ```yaml
   - name: "Install and configure Xorg"
     ansible.builtin.include_role:
       name: ans_role_config_xorg
   ```

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_xorg/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

