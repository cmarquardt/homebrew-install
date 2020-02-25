# Homebrew (un)installer

## Install Homebrew

...but in a place different from `/usr/local` - I do prefer something else, `/opt/homebrew` in this branch.

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/install)"
```

More installation information and options at https://docs.brew.sh/Installation.html.

### Linux and Windows 10 Subsystem for Linux

Install Homebrew on Linux and Windows 10 Subsystem for Linux: https://docs.brew.sh/Linuxbrew.

## Uninstall Homebrew

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/cmarquardt/homebrew-install/feature/install-elsewhere/uninstall)"
```

Download the uninstall script and run `./uninstall --help` to view more uninstall options.
