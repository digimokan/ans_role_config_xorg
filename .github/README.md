# ans_role_config_xorg

Install the base, minimal Xorg display server.

[![Release](https://img.shields.io/github/release/digimokan/ans_role_config_xorg.svg?label=release)](https://github.com/digimokan/ans_role_config_xorg/releases/latest "Latest Release Notes")
[![License](https://img.shields.io/badge/license-MIT-blue.svg?label=license)](LICENSE.md "Project License")

## Table Of Contents

* [Purpose](#purpose)
* [Supported Operating Systems](#supported-operating-systems)
* [Quick Start](#quick-start)
    * [Use From Parent Role As Dependency](#use-from-parent-role-as-dependency)
* [Role Options](#role-options)
* [Contributing](#contributing)

## Purpose

* Install base, minimal [Xorg](https://www.x.org/wiki/) display server.
* Do not install extra Xorg add-on fonts, apps, utilities, etc.

## Supported Operating Systems

* Arch Linux.
* FreeBSD.

## Quick Start

### Use From Playbook

1. Create `requirements.yml` in ansible project root, and add this content:

   ```yaml
   # requirements.yml
   - src: https://github.com/digimokan/ans_role_config_xorg
   ```

2. From the project root directory, install/download the role:

   ```shell
   $ ansible-galaxy install --role-file requirements.yml --roles-path ./roles --force-with-deps
   ```

   * _NOTE:_ `--force-with-deps` _ensures subsequent calls download updates_

3. Include the role like any local role, from the project playbook:

   ```yaml
   # playbook.yml
   - hosts: localhost
     connection: local
     tasks:
       - name: "Install and configure Xorg"
         ansible.builtin.include_role:
           name: ans_role_config_xorg
         vars:
           user_name: "user2"
   ```

## Role Options

Define these _required_ vars for the role:

  * `user_name`: name of primary i3wm user to configure the desktop for

## Contributing

* Feel free to report a bug or propose a feature by opening a new
  [Issue](https://github.com/digimokan/ans_role_config_xorg/issues).
* Follow the project's [Contributing](CONTRIBUTING.md) guidelines.
* Respect the project's [Code Of Conduct](CODE_OF_CONDUCT.md).

