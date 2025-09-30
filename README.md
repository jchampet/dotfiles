# Jerome's dotfiles

![Screenshot of my macOS Terminal](https://github.com/user-attachments/assets/943d4563-7b28-411d-bf82-ea525ab1996b)

This repo contains the dotfiles I use for development on a variety of Linux and macOS systems.
I used to manage those with a combination of manual operations and shell scripts.
Nowadays, I try to use [chezmoi.io](https://www.chezmoi.io) as much as possible to avoid leaking credentials.

## Installation

Install [brew.sh](https://brew.sh/) and type in Terminal:

```
brew update
brew install chezmoi neovim starship
```

Setup `git` with the right credentials. For example: `$GITHUB_USERNAME` and `$GITHUB_TOKEN` if you're still using Github.

Initialize `chezmoi` with this dotfiles repo:

```
chezmoi init --apply https://github.com/$GITHUB_USERNAME/dotfiles.git
```

## Make changes

Edit the thing you'd like to change:

```
chezmoi edit ~/.config/starship.toml
```

Apply the changes:

```
chezmoi -v apply 
```

Commit the changes:

```
chezmoi cd
git add .
git commit -m "Made starship changes"
git push origin main
```
