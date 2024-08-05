# Homebrew (un)installer

## Install Homebrew (on macOS or Linux)

...but in a place different from `/usr/local` - I do prefer something else, `/opt/brew` in this branch.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/install.sh)"
```

This script is a modified version of Homebrew's original installation and de-installation scripts, but using `/opt/brew` as installation prefix for macOS machines. Everything else is unchanged.

General installation information and options: <https://docs.brew.sh/Installation>.

By now, there is also a  `.pkg` installer on [Homebrew's GitHub repository](https://github.com/Homebrew/brew/releases/latest). It does not support alternative installation prefixes on macOS.

If you are running Linux or WSL, [there are some pre-requisite packages to install](https://docs.brew.sh/Homebrew-on-Linux#requirements).

You can set `HOMEBREW_NO_INSTALL_FROM_API` to tap Homebrew/homebrew-core; by default, it will not be tapped as it is no longer necessary.

You can set `HOMEBREW_BREW_GIT_REMOTE` and/or `HOMEBREW_CORE_GIT_REMOTE` in your shell environment to use geolocalized Git mirrors to speed up Homebrew's installation with this script and, after installation, `brew update`.

```bash
export HOMEBREW_BREW_GIT_REMOTE="..."  # put your Git mirror of Homebrew/brew here
export HOMEBREW_CORE_GIT_REMOTE="..."  # put your Git mirror of Homebrew/homebrew-core here
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/install.sh)"
```

The default Git remote will be used if the corresponding environment variable is unset.

If you want to run the Homebrew installer non-interactively without prompting for passwords (e.g. in automation scripts), you can use:

```bash
NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/install.sh)"
```

## Uninstall Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/uninstall.sh)"
```

If you want to run the Homebrew uninstaller non-interactively, you can use:

```bash
NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/uninstall.sh)"
```

If you want to to uninstall Homebrew from a specific prefix (e.g. when migrating from Intel to Apple Silicon processors), download the uninstall script and run it with `--path`:

```
curl -fsSLO https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/uninstall.sh
/bin/bash uninstall.sh --path /usr/local
```

Download the uninstall script and run `/bin/bash uninstall.sh --help` to view more uninstall options.
Run the downloaded script with `/bin/bash uninstall.sh --help` to view more uninstall options.
Download the uninstall script and run `/bin/bash uninstall.sh --help` to view more uninstall options.

## Note

Previous versions of this installer used `/opt/homebrew` as alternative prefix. However, the Homebrew maintainers decided
to use this as root directory for Homebrew on Macs running Apple silicon, and now disallow the installation of Homebrew into
this location. Hence I switched to `/opt/brew`... see https://github.com/Homebrew/brew/issues/9130 for details.
