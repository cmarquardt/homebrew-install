# Homebrew (un)installer

## Install Homebrew (on macOS or Linux)

...but in a place different from `/usr/local` - I do prefer something else, `/opt/homebrew` in this branch.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/master/install.sh)"
```

More installation information and options: https://docs.brew.sh/Installation.

If running Linux or WSL, [there are some pre-requisite packages to install](https://docs.brew.sh/Homebrew-on-Linux#requirements).

## Uninstall Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/master/uninstall.sh)"
```

Download the uninstall script and run `/bin/bash uninstall.sh --help` to view more uninstall options.
