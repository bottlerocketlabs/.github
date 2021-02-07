# README

## About

Bottle Rocket Labs was created to host a number of tools that I use to ease local development

* [pair](https://github.com/bottlerocketlabs/pair) - a tool for remote terminal pair programming
* [localpod](https://github.com/bottlerocketlabs/localpod) - a tool to start a local development container
* [gitlab](https://github.com/bottlerocketlabs/gitlab) - a tool to create gitlab issues
* [dotfiles](https://github.com/bottlerocketlabs/dotfiles) - a tool (as if there wasn't enough) to manage dotfiles
* [rpbcopy](https://github.com/bottlerocketlabs/remote-pbcopy) - a tool to help with copying remote text to the host clipboard over ssh or through tmux - fork

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
brew install bottlerocketlabs/apps/rpbcopy
```

### Debian/Ubuntu package
```sh
curl https://bottlerocketlabs.jfrog.io/artifactory/api/gpg/key/public | sudo apt-key add -
echo "deb https://bottlerocketlabs.jfrog.io/artifactory/deb all main" | sudo tee /etc/apt/sources.list.d/bottlerocketlabs.list
sudo apt-get update

sudo apt-get install -y pair
sudo apt-get install -y gitlab
sudo apt-get install -y dotfiles
sudo apt-get install -y localpod
sudo apt-get install -y rpbcopy
```

### Alpine linux package
```sh
sudo wget -O /etc/apk/keys/bottlerocketlabs.rsa.pub https://bottlerocketlabs.jfrog.io/artifactory/api/security/keypair/public/repositories/alpine
echo "https://bottlerocketlabs.jfrog.io/artifactory/alpine/edge/main" | sudo tee -a /etc/apk/repositories

sudo apk update
sudoa apk add --no-cache pair
sudoa apk add --no-cache gitlab
sudoa apk add --no-cache dotfiles
sudoa apk add --no-cache localpod
sudoa apk add --no-cache rpbcopy
```

### Download binary to current directory
```sh
mkdir -p "${HOME}/bin" && cd "${HOME}/bin"
echo 'PATH="${HOME}/bin:${PATH}"' >> "${HOME}/.profile"

curl 'https://installer-brl.herokuapp.com/pair' | bash
curl 'https://installer-brl.herokuapp.com/gitlab' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles' | bash
curl 'https://installer-brl.herokuapp.com/localpod' | bash
curl 'https://installer-brl.herokuapp.com/rpbcopy' | bash
```

### Download binary to /usr/local/bin as current user
```sh
curl 'https://installer-brl.herokuapp.com/pair!' | bash
curl 'https://installer-brl.herokuapp.com/gitlab!' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles!' | bash
curl 'https://installer-brl.herokuapp.com/localpod!' | bash
curl 'https://installer-brl.herokuapp.com/rpbcopy!' | bash
```

### Download binary to /usr/local/bin with sudo
```sh
curl 'https://installer-brl.herokuapp.com/pair!!' | bash
curl 'https://installer-brl.herokuapp.com/gitlab!!' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles!!' | bash
curl 'https://installer-brl.herokuapp.com/localpod!!' | bash
curl 'https://installer-brl.herokuapp.com/rpbcopy!!' | bash
```

### Install a specific release rather than latest
```sh
# add @<tag> to url after project name eg:
curl 'https://installer-brl.herokuapp.com/pair@v0.0.12!!' | bash
```

See upstream project for further details: https://github.com/jpillora/installer
