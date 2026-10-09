# On Linux:

On Linux (or WSL):

==Note: on the second line here, if you're on COSMIC and want the frosted glass effect to work for emacs, replace `emacs` with `emacs-pgtk`==

```shell
sudo apt update && sudo apt upgrade -y
sudo apt install -y git emacs ripgrep fd-find cmake libtool-bin libvterm-dev
git clone --depth 1 https://github.com/doomemacs/core.git ~/.config/emacs
~/.config/emacs/bin/doom install
```

enter `y` for yes.

```shell
echo 'export PATH="$HOME/.config/emacs/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Now cd into `~/.config`

```shell
rm -rf doom
git clone https://github.com/RockLikeAmadeus/doom-emacs-config.git
mv doom-emacs-config doom
doom sync
```

Finally:

```shell
emacs &
```

## Set up emacs to run as server and client (linux)

Add the emacs daemon to the startup hook (the process differs by desktop environment, but ultimately you just want to run `emacs --daemon`)

Whenever running emacs, be sure and run emacsclient (or `emacsclient -c -a 'emacs'`) when the daemon is running.

# On Windows (not through WSL):

Install emacs using scoop (not chocolatey).

```shell
$ scoop bucket add extras
$ scoop install emacs
$ emacs --version
```

Then clone the doom repo.

```shell
git clone --depth 1 https://github.com/doomemacs/doomemacs.git ~/.config/emacs
```

At this point, make sure you can `cd` into ~/.config and that emacs/bin/doom exists.

The next step must be run in Git Bash. This command takes a long time to run and seems to update in Git Bash infrequently so it appears that it's hanging, but it's likely not.

```shell
~/.config/emacs/bin/doom install
```

Now, still in Git Bash, cd into `~/.config`:

```shell
rm -rf doom
git clone https://github.com/RockLikeAmadeus/doom-emacs-config.git
mv doom-emacs-config doom
doom sync
```

The sync will also take a long time and appear to be hanging.

## Installing necessary custom fonts