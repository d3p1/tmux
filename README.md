<div align=center>

# [TMUX CONFIGURATION]

[![semantic-release: angular](https://img.shields.io/badge/semantic--release-angular-e10079?logo=semantic-release)](https://github.com/semantic-release/semantic-release)
[![Release](https://github.com/d3p1/tmux/actions/workflows/release.yml/badge.svg)](https://github.com/d3p1/tmux/actions/workflows/release.yml)

</div>

## Introduction

Just a configuration for [`tmux`](https://github.com/tmux/tmux) based on this excellent [tutorial](https://www.youtube.com/watch?v=DzNmUNvnB04).

It is used the default [`tmux`](https://github.com/tmux/tmux) configuration with the following customizations:

- It is added the `Ctrl + spacebar` as `prefix` instead of the default `Ctrl + b`, to avoid frequent collision problems with other tool shortcuts.
- It is added the current working directory as the default opened directories for panes.
- It is added [`Tmux Plugin Manager`](https://github.com/tmux-plugins/tpm) to be able to use plugins.

## Usage

First of all, it would be required to install [`tmux`](https://github.com/tmux/tmux) if it is not already installed in your machine:

```
git clone https://github.com/tmux/tmux.git
cd tmux
sh autogen.sh
./configure && make
```

> **Note**
>
> This command requires `autoconf`, `automake` and `pkg-config`.

Then, it is required to install the [`Tmux Plugin Manager`](https://github.com/tmux-plugins/tpm):

```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

Copy the configuration file from this repository:

```
curl -o tmux.conf $XDG_CONFIG_HOME/tmux/tmux.conf
```

> **Note**
>
> In the previous example, the configuration file is copied to `$XDG_CONFIG_HOME/tmux/tmux.conf`, but it can also be copied to `~/.tmux.conf`: `curl -o tmux.conf ~/.tmux.conf`

Finally, connect to `tmux` and run the following command so configuration plugins are installed and environment is reloaded:

```
prefix + I
```

## Changelog

Detailed changes for each release are documented in [`CHANGELOG.md`](./CHANGELOG.md).

## License

This work is published under [MIT License](./LICENSE).

## Author

Always happy to receive a greeting on:

- [LinkedIn](https://www.linkedin.com/in/cristian-marcelo-de-picciotto/)
- [Web](https://d3p1.dev/)