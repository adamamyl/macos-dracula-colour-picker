### MacOS Dracula Color Picker

# Installation

#### Install using Git

If you are a git user, you can install the theme and keep up to date by cloning the repo:

```bash
git clone https://github.com/dracula/macos-dracula-colour-picker.git
cd macos-dracula-colour-picker
```


#### Install manually

Download using the [GitHub `.zip` download](https://github.com/dracula/macos-dracula-colour-picker/archive/main.zip) option and unzip them.


#### Activating theme
 1. Unzip the zip if you downloaded it, or cd to the checkout
 2. Fire up a terminal in the directory, and run the one-liner (you could use finder, if you prefer; you might need to `shift-command-g`  -> `~/Library/Colors` though).
 3. I should advise you to review every copy/paste line you get on the internet, but realise this is often quite futile… but anyhow… 
    1. Review, amend, copy and paste the right one liner for your shell (MacOS default is now zsh).

##### zsh
```zsh
for f in *.clr(N); do [[ ! -e $HOME/Library/Colors/$f ]] && ln -s "$PWD/$f" "$HOME/Library/Colors/$f" && echo "Linked $f"; done
```
---

##### bash

```bash
for f in *.clr; do [ -e "$f" ] || continue; [ ! -e "$HOME/Library/Colors/$f" ] && ln -s "$PWD/$f" "$HOME/Library/Colors/$f" && echo "Linked $f"; done
```
---

Both options make symlinks to the clr files in this repo in ~/Library/Colors, if the files don't already exist. 

Updating this repo (`git pull`) should be all you need to do if/when I update the new colour palettes (which due to idiotic ways of MacOS needs to be done manually)… yes, I've tried in TypeScript, Python, Swift, Base64…