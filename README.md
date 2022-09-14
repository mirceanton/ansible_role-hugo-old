# Ansible Role: Hugo

An Ansible role that installs the Hugo static site generator.

## Requirements

N/A

## Role Variables

### `hugo_version`

**Default**: `0.102.3`

**Required**: no

**Description**: The version of hugo to install. Downloaded from [github releases](https://github.com/gohugoio/hugo/releases)

### `hugo_extended`

**Default**: `true`

**Required**: no

**Description**: Whether or not to download the extended version (as oppposed to the regular version).

### `hugo_arch`

**Default**: `Linux-64bit`

**Required**: no

**Description**: The arch of the executable to download. For example, on a Raspberry Pi this might be set to `Linux-ARM` or `Linux-ARM64`

### `hugo_shell`

**Default**: N/A

**Required**: no

**Description**: The shell for which to set up completion. Leave undefined for no completion to be set up. Can be either `bash`, `fish` or `zsh`.

Dependencies
------------

N/A

Example Playbook
----------------

``` yaml
---
- name: Test playbook
  hosts: all

  roles:
    - role: mirceanton.hugo
      vars:
        hugo_shell: bash
        hugo_version: "0.102.0"
        hugo_extended: false
```

License
-------

MIT

Author Information
------------------

A role by [Mircea-Pavel ANTON (Michael Anthony)](https://mirceanton.com)
