# Homebrew (un)installer

## Install Homebrew (on macOS or Linux)

...but in a place different from `/usr/local` - I do prefer something else, `/opt/brew` in this branch.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/install.sh)"
```

More installation information and options: https://docs.brew.sh/Installation.

If running Linux or WSL, [there are some pre-requisite packages to install](https://docs.brew.sh/Homebrew-on-Linux#requirements).

## Uninstall Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/uninstall.sh)"
```

Download the uninstall script and run `/bin/bash uninstall.sh --help` to view more uninstall options.

## Note

Previous versions of this installer used `/opt/homebrew` as alternative prefix. However, the Homebrew maintainers decided
to use this as root directory for Homebrew on Macs running Apple silicon, and now disallow the installation of Homebrew into
this location. Hence I switched to `/opt/brew`... see https://github.com/Homebrew/brew/issues/9130 for details.
