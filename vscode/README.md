## Get all installed extensions

`code --list-extensions | xargs -L 1 echo code --install-extension`

## Restore on a fresh install

1. In VS Code, press Cmd+Shift+P and run `Shell Command: Install 'code' command in PATH`.
2. Paste the contents of `extensions.txt` into a terminal.
3. From this folder, copy the config files into place:
   `cp settings.json keybindings.json mcp.json ~/Library/Application\ Support/Code/User/`
4. Let held keys repeat in the Vim extension:
   `defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false`
5. The Sanity MCP token is not stored in `mcp.json`. VS Code asks for it the first time the server starts.
