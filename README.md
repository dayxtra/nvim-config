1. ### Install nvim

Install from package manager

```bash
sudo apt install neovim \
-y
```
>Check verison! Should be >= 0.7.0

OR build from source code *(Prefered)* 
```bash
sudo apt install git ninja-build gettext cmake unzip curl \
-y
```

```bash
git clone https://github.com/neovim/neovim
```

```bash
cd neovim
git checkout stable
```

```bash
make CMAKE_BUILD_TYPE=Release
sudo make install
```
2. ### Install pyright


```bash
# Prefered
sudo apt install npm -y && sudo npm install -g pyright
```
OR
```bash
pip3 install pyright
```
3. ### Install vim-plug


```bash
mkdir -p ~/.config/nvim
```

```bash
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```
4. ### Configure nvim


```bash
nvim ~/.config/nvim/init.vim
```
[Config](init.vim)

Type `:w` to save file.

Type `:so %` to apply config *(ignore errors)*.

Type `:PlugInstall` to install plugins.