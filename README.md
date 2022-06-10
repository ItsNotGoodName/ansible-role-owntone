# ansible-role-owntone

Install and configure [OwnTone](https://github.com/owntone/owntone-server) on Debian and Ubuntu.

## Requirements

N/A

## Role Variables

Change OwnTone version with `owntone_version` variable.

```yaml
owntone_version: "28.4"
```

Configure OwnTone when the variable `owntone_config` is defined.

```yaml
owntone_config: |
  # owntone config from /etc/owntone.conf
```

Enable or disable OwnTone features.

```yaml
owntone_enable_chromecast: false # Enable chromecast
owntone_enable_libspotify: false # Enable libspotify
owntone_enable_pulseaudio: false # Enable pulseaudio

owntone_disable_spotify: false # Disable built-in spotify
owntone_disable_playerwebui: false # Disable web-ui
owntone_disable_livewebui: false # Disable websockets for web-ui
```

Remove static audio when not playing anything. Only works when using ALSA with Intel Audio.

```yaml
owntone_alsa_intel_audio_static_fix: true
```

## Tags

Only run the OwnTone role with the `owntone` tag.

```
ansible-playbook main.yml --tags owntone
```

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
