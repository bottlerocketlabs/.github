# README
Installation instructions for bottlerocketlabs applications

Applications are available for install via homebrew or curling a script into bash


## Homebrew Formulae
```sh
brew install bottlerocketlabs/apps/pair
brew install bottlerocketlabs/apps/gitlab
brew install bottlerocketlabs/apps/dotfiles
brew install bottlerocketlabs/apps/localpod
brew install bottlerocketlabs/apps/pbcopy
```

## Download binary to current directory
```sh
mkdir -p "${HOME}/bin" && cd "${HOME}/bin"
echo 'PATH="${HOME}/bin:${PATH}"' >> "${HOME}/.profile"

curl 'https://installer-brl.herokuapp.com/pair' | bash
curl 'https://installer-brl.herokuapp.com/gitlab' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles' | bash
curl 'https://installer-brl.herokuapp.com/localpod' | bash
curl 'https://installer-brl.herokuapp.com/pbcopy' | bash
```

## Download binary to /usr/local/bin as current user
```sh
curl 'https://installer-brl.herokuapp.com/pair!' | bash
curl 'https://installer-brl.herokuapp.com/gitlab!' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles!' | bash
curl 'https://installer-brl.herokuapp.com/localpod!' | bash
curl 'https://installer-brl.herokuapp.com/pbcopy!' | bash
```

## Download binary to /usr/local/bin with sudo
```sh
curl 'https://installer-brl.herokuapp.com/pair!!' | bash
curl 'https://installer-brl.herokuapp.com/gitlab!!' | bash
curl 'https://installer-brl.herokuapp.com/dotfiles!!' | bash
curl 'https://installer-brl.herokuapp.com/localpod!!' | bash
curl 'https://installer-brl.herokuapp.com/pbcopy!!' | bash
```

## Install a specific release rather than latest
```sh
# add @<tag> to url after project name eg:
curl 'https://installer-brl.herokuapp.com/pair@v0.0.12!!' | bash
```

See upstream project for further details: https://github.com/jpillora/installer
