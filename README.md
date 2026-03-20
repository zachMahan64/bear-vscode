<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/bear-language/bear-vscode/blob/main/images/bear-logo-text-dark.png?raw=true">
    <source media="(prefers-color-scheme: light)" srcset="https://github.com/bear-language/bear-vscode/blob/main/images/bear-logo-text-light.png?raw=true">
    <img alt="The Bear Programming Language"
         src="https://raw.githubusercontent.com/zachMahan64/bear-vscode/refs/heads/main/images/bear-logo.png"
         width="50%">
  </picture>

</div>

# The Official VSCode Extension for Bear

Features
--------
- Syntax highlighting for the Bear language
- More planned!

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
4. install it via: `code --install-extension bear-language-0.0.1.vsix` or via VSCode UI: Extensions → `...` → Install from VSIX.
    - to get the `code` command, you need to install vscode CLI or enable it within VSCode by running ctrl+shift+p / cmd+shift+p -> shell command: install code command in path  

