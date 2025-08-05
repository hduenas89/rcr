```markdown
# Rice Cooker (`rcr`)

Rice Cooker (`rcr`) is a vibe-coded command-line tool for Arch Linux to create configuration scripts by logging commands, adding comments, bundling packages, and reordering entries.
Perfect for ricing (customizing) your Arch setup with reproducible scripts.
Warning: This has not been extensively tested, is still in its early stages and will be buggy. I'm currently trying it out on a virtualbox installation.

## Features
- Log executed commands (`-a`) or manually add commands (`-n`).
- Add comments to document commands (`-c`).
- Bundle packages from Arch repos, AUR, or Flatpak (`-b`).
- Interactively reorder commands with comments via TUI (`-r`).
- Edit (`-e`) or preview (`-p`) scripts.
- Custom script paths (`-f`).

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/hduenas89/rcr.git
   cd rcr
   ```
2. Move the script to `~/.local/bin`:
   ```bash
   mkdir -p ~/.local/bin
   cp rcr ~/.local/bin/rcr
   chmod +x ~/.local/bin/rcr
   ```
3. Ensure `~/.local/bin` is in your `$PATH`:
   ```bash
   echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc
   ```
4. Install `dialog` for reordering:
   ```bash
   sudo pacman -S dialog
   ```

## Usage
```bash
rcr --init                    # Initialize a new script (~/.rice-cooker/config.sh)
rcr -a                        # Add the last command
rcr -c                        # Add a comment
rcr -n                        # Add a command without running
rcr -b arch i3 polybar        # Bundle Arch packages
rcr -r                        # Reorder commands interactively
rcr -e                        # Edit the script
rcr -p                        # Preview the script
rcr -f ~/my-script.sh -a      # Use a custom script
rcr --help                    # Show help
```

### Example
```bash
rcr --init
sudo pacman -S i3
rcr -ac  # Comment: "Install i3 window manager"
rcr -n   # Command: "mkdir -p ~/.config/i3"
rcr -b aur yay
rcr -r   # Reorder commands
```

Output script (`~/.rice-cooker/config.sh`):
```bash
#!/bin/bash
# Rice Cooker Configuration Script
# Created on: Sat Aug 02 21:25:00 2025
# By: user
# Install i3 window manager
sudo pacman -S i3
mkdir -p ~/.config/i3
# Bundle: aur packages (yay)
sudo pacman -S --needed git base-devel
git clone https://aur.archlinux.org/yay.git /tmp/yay
cd /tmp/yay && makepkg -si
yay -S --needed yay
```

## Dependencies
- `bash`: For running the script.
- `dialog`: For the interactive reordering feature (`-r`).
- `pacman`: For Arch package management.
- Optional: `yay` (or another AUR helper) for AUR bundles, `flatpak` for Flatpak bundles.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License
MIT License. See [LICENSE](LICENSE) for details.
```
