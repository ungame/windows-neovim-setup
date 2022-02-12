# WINDOWS NEOVIM SETUP

## Donwload

- https://github.com/neovim/neovim/releases/

## Configurações

- Abrir o terminal

- Entrar no diretório `C:\Users\{SEU_USUARIO}\AppData\Local`:

```cmd
cd C:\Users\{SEU_USUARIO}\AppData\Local
```

- Criar o diretório `nvim`:

```cmd
mkdir nvim
```

- Entrar no diretório `nvim`:

```cmd
cd nvim
````

- Criar o arquivo `init.vim` e adicionar as configurações básicas:

```vim
syntax on            " Enable syntax highlight
set nu               " Enable line numbers
set tabstop=4        " Show existing tab with 4 spaces width
set softtabstop=4    " Show existing tab with 4 spaces width
set shiftwidth=4     " When indenting with '>', use 4 spaces width
set expandtab        " On pressing tab, insert 4 spaces
set smarttab         " insert tabs on the start of a line according to shiftwidth
set smartindent      " Automatically inserts one extra level of indentation in some cases
set hidden           " Hides the current buffer when a new file is openned
set incsearch        " Incremental search
set ignorecase       " Ingore case in search
set smartcase        " Consider case if there is a upper case character
set cmdheight=2      " Give more space for displaying messages
set updatetime=100   " Time in miliseconds to consider the changes
set encoding=utf-8   " The encoding should be utf-8 to activate the font icons
```

## Plugins

- Instalar: https://github.com/junegunn/vim-plug

```cmd
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
```

## Themes

Para instalar temas via Plug basta saber o nome de usuário do github, e o nome do repositório.

- Repositório: https://github.com/rafi/awesome-vim-colorschemes
- Abrir o arquivo init.vim
- Adicionar o plugin no inicio do arquivo

```vim
call plug#begin()
Plug 'rafi/awesome-vim-colorschemes'
call plug#end()
```

- Para instalar o thema é necessário entrar no modo Normal do nvim e executar o comando:

```vim
:PlugInstall
```

- Após instalar o plugin agora é só escolher um tema e adicionar no arquivo `init.vim`, ex:

```vim
colorscheme gruvbox
```

---

- Arquivo completo:

```vim
call plug#begin()
Plug 'rafi/awesome-vim-colorschemes'
call plug#end()

syntax on            " Enable syntax highlight
set nu               " Enable line numbers
set tabstop=4        " Show existing tab with 4 spaces width
set softtabstop=4    " Show existing tab with 4 spaces width
set shiftwidth=4     " When indenting with '>', use 4 spaces width
set expandtab        " On pressing tab, insert 4 spaces
set smarttab         " insert tabs on the start of a line according to shiftwidth
set smartindent      " Automatically inserts one extra level of indentation in some cases
set hidden           " Hides the current buffer when a new file is openned
set incsearch        " Incremental search
set ignorecase       " Ingore case in search
set smartcase        " Consider case if there is a upper case character
set cmdheight=2      " Give more space for displaying messages
set updatetime=100   " Time in miliseconds to consider the changes
set encoding=utf-8   " The encoding should be utf-8 to activate the font icons
colorscheme gruvbox
```
