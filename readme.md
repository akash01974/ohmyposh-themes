# NeonGrid Oh My Posh Theme

## Preview

![NeonGrid preview](image.png)

## Requirements

- Oh My Posh
- Nerd Font or a patched font with Powerline/nerd icons
- Konsole terminal emulator
- Bash shell (or another supported shell)
- `~/bin` available in `PATH` if installing Oh My Posh there

## Installation

Step 1: Install Oh My Posh

Oh My Posh is the tool that makes your terminal look cool. Run this command to install it in your home bin folder:

```bash
curl -s https://ohmyposh.dev/install.sh | bash -s -- -d ~/bin
```

If you want to install it in the default system location instead, use this:

```bash
curl -s https://ohmyposh.dev/install.sh | bash -s
```

Step 2: Check if Oh My Posh is installed correctly

After installation, verify it works by checking the version:

```bash
oh-my-posh --version
```

You should see the version number if it's installed properly.

Step 3: Install the required fonts

Icons and symbols need special fonts. Install the recommended font set with:

```bash
oh-my-posh font install
```

If you prefer a specific font, try JetBrains Mono Nerd Font, which includes all the icons.

Step 4: Get the theme files

Download this theme from GitHub:

```bash
git clone https://github.com/akash01974/ohmyposh-themes.git ~/ohmyposh-theme
cd ~/ohmyposh-theme
```

Step 5: Set up the theme file

Copy the theme file to the right place:

```bash
mkdir -p ~/.config/ohmyposh/themes
cp NeonGrid.json ~/.config/ohmyposh/themes/
```

## Configuration


Enable the theme in your shell by adding the init line to `~/.bashrc`:

```bash
eval "$(oh-my-posh init bash --config ~/.config/ohmyposh/themes/NeonGrid.json)"
```

If you want to generate the exact shell initialization snippet, run:

```bash
oh-my-posh get shell
```

Then add the output to your shell config file.

After editing:

```bash
source ~/.bashrc
```

## File Structure

- Theme file: NeonGrid.json
- Recommended theme directory: `~/.config/ohmyposh/themes/`
- Legacy theme directories:
  - `~/.poshthemes`
  - `/usr/share/oh-my-posh/themes/`

## Customization

To customize the theme:

- Edit `~/.config/ohmyposh/themes/NeonGrid.json`
- Change colors, segments, icons, or text templates
- Reload your shell after saving changes:

```bash
source ~/.bashrc
```

If you use another shell, replace `bash` with `zsh` or `fish` in the `oh-my-posh init` command.

## Troubleshooting

- Icons not showing?
  - Make sure Konsole is using a Nerd Font such as JetBrains Mono Nerd Font.
  - Restart Konsole after installing fonts.

- Theme not loading?
  - Confirm the theme path is correct:
    `~/.config/ohmyposh/themes/NeonGrid.json`
  - Verify the shell init line is present in `~/.bashrc`.

- `oh-my-posh` command not found?
  - Ensure `~/bin` is in your `PATH` if installed there:
    `export PATH="$HOME/bin:$PATH"`

## Notes

- This theme is intended for Konsole with a patched Powerline/Nerd Font.
- If you are using a different shell, adapt the init command accordingly.
- The theme file should live alongside your Oh My Posh config files.

## License

MIT