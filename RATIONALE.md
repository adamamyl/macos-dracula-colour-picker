# Rationale for a Separate Repo

The original [macos-color-picker](https://github.com/dracula/macos-color-picker) repo is **broken/unmaintained**:

- The Homebrew tap `dracula/homebrew-install` fails with modern Homebrew.
- The generator script (`json-clr.js`) depends on the deprecated `dracula-yaml-json` tool.
- Running with Node.js fails (`ObjC not defined`) — the script is JXA, not Node.
- No pre-generated `.clr` file is included, and instructions are outdated.

This repo provides:

- Manually created clrs on MacOS, so they should import for you (and me on other machines).
- No reliance on broken Homebrew taps or external generators.
- One-liners for symlinking the palettes to `~/Library/Colors` for MacOS users.