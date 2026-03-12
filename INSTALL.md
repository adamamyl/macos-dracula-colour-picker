# Installation

```bash
git clone https://github.com/adamamyl/macos-dracula-colour-picker.git
cd macos-dracula-colour-picker
```

Review, amend, copy and paste the right one liner for your shell (MacOS default is now zsh).

### zsh
```zsh
for f in *.clr(N); do [[ ! -e $HOME/Library/Colors/$f ]] && ln -s "$PWD/$f" "$HOME/Library/Colors/$f" && echo "Linked $f"; done
```

## OR

### bash

```bash
for f in *.clr; do [ -e "$f" ] || continue; [ ! -e "$HOME/Library/Colors/$f" ] && ln -s "$PWD/$f" "$HOME/Library/Colors/$f" && echo "Linked $f"; done
```

Both options make symlinks to the clr files in this repo in ~/Library/Colors, if the files don't already exist. Updating this repo (`git pull`) should be all you need to do if/when I update the new colour palettes (which due to idiotic ways of MacOS needs to be done manually). Yes, I've tried in TypeScript, Python, Swift, Base64…