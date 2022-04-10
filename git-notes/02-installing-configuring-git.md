# Installing & Configuring Git

## Installing Git
- If you use windows, go to https://gitforwindows.org/ to download.

- If you use Mac OS X, go to https://git-scm.com/download/mac to download.

- Some IDE or code editor, such as Sublime Text, VS Code, etc, has had git installed. Some of them provide user-friendly graphical interface, but here we only discuss about command line version of git.

- Now assuming that you have the experience in working with console, let's preceed with installation.

```bash
#On Debian / Termux / Ubuntu / Mint / Elementary OS / Ziron / Linux Lite / other distributions based on Debian.
sudo apt install git-all

#On Fedora / Red Hat Enterprise Linux / CentOS Stream
sudo dnf install git-all

#On Gentoo
sudo emerge --ask --verbose dev-vcs/git

#On Arch Linux / Manjaro / Endeavour OS / other distributions based on Arch Linux.
pacman -S git

#On OpenSuSE
zypper install git

#On Nix
nix-env -i git

#On FreeBSD
pkg install git
```

## Configure Git

- Introduce yourself to git! Tell git your user name, email and favorate editor. Here I examplify myself:

```bash
git config --global user.name "xforcevesa"
git config --global user.email "nomodeset@qq.com"
git config --global core.editor gedit
# You can use absolute path to specify your favorate editor
git config --global core.editor "C:\\Program Files\\emacs\\emacs.exe"
```

- Set main as your default development branch.

```bash
git config --global init.defaultBranch main
```

- View all of your settings and where they are coming from using:

```bash
git config --list --show-origin
```

## Tip
- Provided that you have question about usage of some subcommand, use these commands:

```bash
git help <subcommand>
git <subcommand> --help
man git-<subcommand>
```

## Conclusion

- Now we have successfully installed and configured git.

- From now on, I assume that your development environment is Ubuntu GNU/Linux 21.10 running on Intel Core™ i7 7700K.
