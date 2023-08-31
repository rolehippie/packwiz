# packwiz

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/packwiz)
[![General Workflow](https://github.com/rolehippie/packwiz/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/packwiz/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/packwiz/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/packwiz/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/packwiz/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/packwiz/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/packwiz)](https://github.com/rolehippie/packwiz/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.packwiz-blue)](https://galaxy.ansible.com/rolehippie/packwiz)

Ansible role to install packwiz minecraft modpack builder.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [packwiz_arch](#packwiz_arch)
  - [packwiz_download](#packwiz_download)
  - [packwiz_force](#packwiz_force)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### packwiz_arch

Architecture of the static binary

#### Default value

```YAML
packwiz_arch: "{{ 'ARM' if ansible_architecture == 'aarch64' else 'x86' }}"
```

### packwiz_download

URL to the archive of the release to install

#### Default value

```YAML
packwiz_download: https://nightly.link/packwiz/packwiz/workflows/go/main/Linux%2064-bit%20{{
  packwiz_arch }}.zip
```

### packwiz_force

Force reinstallation of binary

#### Default value

```YAML
packwiz_force: false
```

## Discovered Tags

**_packwiz_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
