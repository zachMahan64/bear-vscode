# Bear Language VSCode Extension

Syntax highlighting for the Bear language.

## Install locally

1. Copy the `bear-vscode/` folder into your VSCode extensions directory:
   - **Linux/macOS**: `~/.vscode/extensions/bear-language/`
   - **Windows**: `%USERPROFILE%\.vscode\extensions\bear-language\`
2. Restart VSCode (or run `Developer: Reload Window` from the command palette).
3. Open any `.bear` or `.br` file and highlighting will apply automatically.

### `.vsix` package install
1. install the VSCode Extension CLI: `npm install -g @vscode/vsce`
2. From inside the extension folder: `vsce package`
3. This produces `bear-language-0.0.1.vsix`, or whatever the current version is.
4. install it via: `code --install-extension bear-language-0.0.1.vsix`
   or via VSCode UI: Extensions → `...` → Install from VSIX.

