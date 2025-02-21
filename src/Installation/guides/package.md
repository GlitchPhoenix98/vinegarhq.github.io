# Installation from your package manager

### Arch Linux or derivatives (AUR)

To install Vinegar, run the following commands:

```sh
git clone https://aur.archlinux.org/vinegar.git
cd vinegar
makepkg -si
```

### Gentoo

Firstly, make sure the repository module for eselect is installed:
```sh
emerge app-eselect/eselect-repository
```

Then you will need to add the Vinegar overlay:

```sh
eselect repository add "vinegar" git https://github.com/vinegarhq/ebuild.git
emaint sync
```
And emerge the package:
```sh
emerge -av games-util/vinegar
```

Alternatively, you can use the live ebuild by creating a `/etc/portage/package.accept_keywords/vinegar` file with the following content:
```
games-util/vinegar **
```
