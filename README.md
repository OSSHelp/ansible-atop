# atop

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/atop/status.svg)](https://drone.osshelp.ru/ansible/atop)

Simple Ansible role for atop installation.

## Usage (example)

```yaml
    - role: atop
      atop_daemon_interval: 60
```

## Available parameters

### Main

Short description here.

| Param | Description |
| -------- | -------- |
| atop_packages | List of packages to install. By default the role installs atop and acct. |
| atop_daemon_interval | How often the accounting records will be saved on disk (in seconds). |
| atop_memory_limit | Memory limit for service in bytes, by default: 1073741824 (1Gb). |

### atop_paths

List of default paths, do not change them with no reason.

| Param | Description |
| -------- | -------- |
| systemd_main_service | Path to main systemd unit. |
| systemd_rotate_timer |  Path to atop-rotate timer unit. |
| systemd_rotate_service |  Path to atop-rotate service unit. |
| binary_path | Path to atop binary. |
| log_dir | Path to atop log directory. |
| env_file | Path to atop environment file. |

### Misc

| Param | Description |
| -------- | -------- |
| atop_user_interval, atop_flags, atop_maxlineintf | Params used for /root/.atoprc generation, do not change them. |
| atop_disable_systemd_configuration | With this param you can disable the whole systemd configuration if needed. |
| atop_role_test_mode | Param to properly test role in builds, do not use it in playbooks. |

## Useful links

- [Official documentation](https://www.atoptool.nl/download/man_atop-1.pdf)
- [Our article](https://oss.help/kb647)

## TODO

- Setup tests via Molecule >= 2.22+ and VMs at DigitalOcean

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
