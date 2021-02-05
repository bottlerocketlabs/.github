# README

## About

Bottle Rocket Labs was created to host a number of tools that I use to ease local development

* [pair](https://github.com/bottlerocketlabs/pair) - a tool for remote terminal pair programming
* [localpod](https://github.com/bottlerocketlabs/localpod) - a tool to start a local development container
* [gitlab](https://github.com/bottlerocketlabs/gitlab) - a tool to create gitlab issues
* [dotfiles](https://github.com/bottlerocketlabs/dotfiles) - a tool (as if there wasn't enough) to manage dotfiles
* [pbcopy](https://github.com/bottlerocketlabs/remote-pbcopy) - a tool to help with copying remote text to the host clipboard over ssh or through tmux - fork

Everything here was built on the shoulders of giants using a number of other amazing projects hard work:
* [pion/webrtc](https://github.com/pion/webrtc)
* [maxmcd/webtty](https://github.com/maxmcd/webtty)
* [docker](https://github.com/moby/moby)
* [go-git](https://github.com/go-git/go-git)
* [xanzy/go-gitlab](https://github.com/xanzy/go-gitlab)
* [goreleaser](https://github.com/goreleaser/goreleaser)
* [jpillora/installer](https://github.com/jpillora/installer)

Hopefully there is something useful here for you

## Install instructions
Installation instructions for bottlerocketlabs applications

Applications are available for install via homebrew or curling a script into bash

### Homebrew Formulae
```sh
# Should work on mac, linux or windows with wsl2
brew install bottlerocketlabs/apps/pair
brew install bottlerocketlabs/apps/gitlab
brew install bottlerocketlabs/apps/dotfiles
brew install bottlerocketlabs/apps/localpod
brew install bottlerocketlabs/apps/pbcopy
```

### Download binary to current directory
```sh
mkdir -p "${HOME}/bin" && cd "${HOME}/bin"
echo 'PATH="${HOME}/bin:${PATH}"' >> "${HOME}/.profile"

curl 'https://installer-brl.herokuapp.com/pair' | bash
curl 'https://installer-brl.herokuapp.com/gitlab' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles' | bash
curl 'https://installer-brl.herokuapp.com/localpod' | bash
curl 'https://installer-brl.herokuapp.com/pbcopy' | bash
```

### Download binary to /usr/local/bin as current user
```sh
curl 'https://installer-brl.herokuapp.com/pair!' | bash
curl 'https://installer-brl.herokuapp.com/gitlab!' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles!' | bash
curl 'https://installer-brl.herokuapp.com/localpod!' | bash
curl 'https://installer-brl.herokuapp.com/pbcopy!' | bash
```

### Download binary to /usr/local/bin with sudo
```sh
curl 'https://installer-brl.herokuapp.com/pair!!' | bash
curl 'https://installer-brl.herokuapp.com/gitlab!!' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles!!' | bash
curl 'https://installer-brl.herokuapp.com/localpod!!' | bash
curl 'https://installer-brl.herokuapp.com/pbcopy!!' | bash
```

### Install a specific release rather than latest
```sh
# add @<tag> to url after project name eg:
curl 'https://installer-brl.herokuapp.com/pair@v0.0.12!!' | bash
```

See upstream project for further details: https://github.com/jpillora/installer
