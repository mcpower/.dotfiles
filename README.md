# .dotfiles

Opinionated dotfiles.

To install on Ubuntu, probably Debian too:

```zsh
sudo apt install zsh git rustup
# Don't forget to set up your GitHub SSH keys!
git clone --recurse-submodules --shallow-submodules git@github.com:mcpower/.dotfiles.git ~/.dotfiles
~/.dotfiles/install
chsh -s $(which zsh)

# install jj
sudo apt install rustup
rustup toolchain install stable
cargo install cargo-binstall
cargo binstall --strategies crate-meta-data jj-cli

jj git init --colocate ~/.dotfiles
jj b track --remote=origin main
```

If you don't intend on working on this repo and just want a read-only version:

```zsh
sudo apt install zsh git
git clone --recurse-submodules --shallow-submodules --depth=1 https://github.com/mcpower/.dotfiles.git ~/.dotfiles
~/.dotfiles/install
chsh -s $(which zsh)
```
