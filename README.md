# Starship present: StarKitty

[Starship](https://starship.rs) Promt present that features Material 3 generated colors powered by [Matugen](https://github.com/InioX/matugen.git).

This present uses matugen to sync your terminal promt colors with your wallpaper or choosen color palette.


## Preview

| Screenshot |
|------------|
|<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/242cc5b8-3a65-4866-89ff-829bd6bd3c39" />|
|<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/2d51e743-2ff2-4cb5-bbd0-669e921ba6c2" />

## Prerequisites
Make sure you have following dependencies installed on your system:
1. **Starship Prompt**
  ```bash
  #install via corss-platform script
  curl -sS https://starship.rs/install.sh | sh
```
```bash
#install via your distro package manager (for example: for Arch Linux)
sudo pacman -S starship
```
check out [Starship installation](https://starship.rs/installing/). 

2. **Matugen**
```bash
#install via your distro package manager (for example: for Arch Linux)
sudo pacman -S matugen
```

## Installation and Setup
### Clone the present
Clone the repository 


```bash
git clone https://github.com/aokxmi/starkitty.git
cd starkitty
```

### Configure the template 

Move the template into your matugen templates folder

```bash
mkdir -p ~/.config/matugen/templates
cp matugen/templates/starship.toml
~/.config/matugen/templates/starship.toml
```

Add the configuration block to matugen config `~/.config/matugen/config.toml`
```toml
[templates.starship]
input_path = '~/.config/matugen/templates/starship.toml'
output_path = '~/.config/starship.toml'
```

### 3. Enable Starship in Your Shell
Add the initialization hook to your shell configuration file.

* **Bash** (`~/.bashrc`):
  ```bash
  eval "$(starship init bash)"
  ```
* **Zsh** (`~/.zshrc`):
  ```bash
  eval "$(starship init zsh)"
  ```
* **Fish** (`~/.config/fish/config.fish`):
  ```fish
  starship init fish | source
  ```

### 3. Generate Your Theme
Run Matugen to make populate your `starship.toml`:
```bash
# Generate from wallpaper
matugen image /path/to/your/wallpaper.jpg

# Generate using a specific hex color
matugen color #3b5998
```

---




