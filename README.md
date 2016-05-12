[![Slack Room][slack-badge]][slack-link]
[slack-link]: https://fisherman-wharf.herokuapp.com/
[slack-badge]: https://fisherman-wharf.herokuapp.com/badge.svg

## Fishface

Simple prompt that shows an ASCII fish instead of a prompt.

![Screenshot](https://cloud.githubusercontent.com/assets/10598847/15026896/6ea5d9ec-1249-11e6-9144-58fccbc28b72.png)

### Fish colors

(in order of precedence)

| Color | Meaning |
| --- | --- |
| Light Red | Last command exited non-zero |
| Peach | There are background jobs running |
| Yellow | Git repo dirty |
| Green | In a git repo |
| Light Blue | In Python virtualenv |
| Purple | Running as root |
| Orange | Directory not writable |
| Blue | Normal |

### Install

With [fisherman](https://github.com/fisherman/fisherman)

```
fisher randomdude999/theme-fishface
```

### Configuration

You can override some of the following default options in your *config.fish*:

```fish
set -g fishface_fish # Default is '><((("> '

# Status, jobs, git, etc

set -g fishface_display_status 1
set -g fishface_display_jobs 1
set -g fishface_display_git 1
set -g fishface_display_git_dirty 1
set -g fishface_display_virtual_env 1
set -g fishface_display_root 1
set -g fishface_display_readonly 1

# Colors

set -g fishface_default_color
set -g fishface_status_color
set -g fishface_jobs_color
set -g fishface_git_color
set -g fishface_git_dirty_color
set -g fishface_virtual_env_color
set -g fishface_root_color
set -g fishface_readonly_color
```

You can also disable particular things, for example if you don't want the fish to change color when a virtualenv is active, you can set `set -g fishface_display_virtual_env 0`.

### Authors

Originally by [@krisleech](https://github.com/krisleech), improved by [@randomdude999](https://github.com/randomdude999)

