# ansible-role-owntone

Install and configure [OwnTone](https://github.com/owntone/owntone-server) on Debian 11.

## Requirements

N/A

## Role Variables

Change OwnTone version with `owntone_version` variable.

```yaml
owntone_version: "28.3"
```

Configure OwnTone when the variable `owntone_config` is defined.

```yaml
owntone_config: |
  # owntone config from /etc/owntone.conf
```

Pass arguments to configure command when building OwnTone. List of arguments at [OwnTone Install Docs](https://github.com/owntone/owntone-server/blob/master/INSTALL.md#quick-version-for-debianubuntu-users).

```yaml
owntone_configure_args: ""
```

## Tags

Reinstall OwnTone with the `owntone_reinstall` tag.

```
ansible-playbook main.yml --tags owntone_reinstall
```

## Dependencies

N/A

## Example Playbook

```yaml
- hosts: all
  roles:
    - itsnotgoodname.owntone
```

## License

MIT

## Author Information

ItsNotGoodName
