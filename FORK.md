# Fork Notes

This is a fork of [omarchy](https://github.com/basecamp/omarchy) with all third-party closed-source apps removed.

## Upstream Sync

```bash
git remote add upstream https://github.com/basecamp/omarchy.git  # one-time setup
git fetch upstream
git merge upstream/main
```

## Changes From Upstream

### Removed from `install/omarchy-base.packages`
- `1password-beta`, `1password-cli`
- `claude-code`
- `obsidian`
- `signal-desktop`
- `spotify`
- `typora`

### Cleared `install/packaging/webapps.sh`
All web apps removed: HEY, Basecamp, WhatsApp, Google Photos/Contacts/Messages/Maps, ChatGPT, YouTube, GitHub, X, Figma, Discord, Zoom, Fizzy.

### Deleted install scripts
- `bin/omarchy-install-dropbox`
- `bin/omarchy-install-nordvpn`
- `bin/omarchy-install-geforce-now`
- `bin/omarchy-install-steam`
- `bin/omarchy-install-vscode`

### `bin/omarchy-menu`
Removed from install menus: Dropbox, NordVPN, Steam, NVIDIA GeForce NOW, VSCode.

### `config/hypr/bindings.conf`
Removed keybindings for: Spotify, Signal, Obsidian, Typora, 1Password, and all webapp shortcuts.

### `default/hypr/bindings.conf`
Removed keybindings for: Obsidian, Signal, 1Password.

### Deleted webapp icons
All files under `applications/icons/` for the removed web apps, plus `applications/typora.desktop`.

## After Each Upstream Merge

Re-check and re-apply the above removals if upstream re-adds them, particularly in:
- `install/omarchy-base.packages`
- `install/packaging/webapps.sh`
- `bin/omarchy-menu`
- `config/hypr/bindings.conf`
