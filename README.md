# ametrine-hooks

AmetrineOS pacman hooks

Pacman hooks to prevent the system from reverting itself into vanilla Arch.

| File name                 | Description                                                                 |
| :------------------------ | :-------------------------------------------------------------------------- |
| ametrine-hooks-runner     | Fixes files like `os-release`, `lsb-release`, `issues` for EndeavourOS.     |
| ametrine-hooks.hook       | Runs `ametrine-hooks-runner` after the `ametrine-hooks` package is updated. |
| ametrine-lsb-release.hook | Runs `ametrine-hooks-runner` after package `lsb-release` has been updated.  |
| ametrine-os-release.hook  | Runs `ametrine-hooks-runner` after package `filesystem` has been updated.   |

Forked from [EndeavourOS pacman hooks](https://github.com/endeavouros-team/PKGBUILDS/tree/master/eos-hooks)
