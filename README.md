# Ansible Role: gum

[![CI](https://github.com/sgaunet/ansible-role-gum/workflows/CI/badge.svg?event=push)](https://github.com/sgaunet/ansible-role-gum/actions?query=workflow%3ACI)

An Ansible Role that installs [gum][https://github.com/charmbracelet/gum] on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    gum_version: "latest"     # Version of gum to install. Use "latest" to install the latest version.
    gum_bin_path: "/usr/local/bin"
    gum_tmp_directory: "{{ lookup('env', 'TMPDIR') | default('/tmp', true) }}"
    gum_os: "linux"
    gum_arch: "amd64"

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - sgaunet.gum
```

## License

MIT
