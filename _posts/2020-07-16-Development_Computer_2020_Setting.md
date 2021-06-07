---
layout: post
title: 2020 My Computer Setting
tags: Setting
comments: true
---

2020년 컴퓨터 세팅

## APP
---
- IDE

    [Itrem2](https://www.iterm2.com)

    [Visual Studio Code](https://code.visualstudio.com)

    [Octave](https://www.gnu.org/software/octave/)

    [Xcode](https://apps.apple.com/kr/app/xcode/id497799835?mt=12)

- Development tools

    [Dash](https://kapeli.com/dash)

    [GitKraken](https://www.gitkraken.com)

    [Cakebrew](https://www.cakebrew.com)

    [Postman](https://www.postman.com)

    [Station](https://getstation.com)

    [DBeaver](https://dbeaver.io)

    [SnippetsLab](https://apps.apple.com/us/app/snippetslab/id1006087419)

- Virtualization tools

    [VirtualBox](https://www.virtualbox.org)

    [Docker](https://www.docker.com)

- Design tools

    [Kicad](https://kicad-pcb.org)

    [Figma](https://www.figma.com)

    [Zeplin](https://zeplin.io)

- Mail

    [Spark](https://sparkmailapp.com)


## Terminal
---
### Vim
---
#### Vundle Install
``` shell
$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
#### .vimrc Setting
``` shell
$ vi .vimrc
```
.vimrc 추가
``` bash
" === Indent ===
set cindent
set autoindent
set smartindent
set tabstop=4
set shiftwidth=4

" === View ===
set number
set ruler
set title
set showmatch
set linebreak
set wrap
set background=dark
set guifont=NanumGothicCoding:h12:cHANGEUL

" === search ===
set hlsearch
set ignorecase
set incsearch

" === Edit ===
set backspace=eol,start,indent
set history=1000
set fencs=ucs-bom,utf-8,euc-kr,latin1
set fileencoding=utf-8
set nobackup

" === Color ===
syntax on

" === Vundle config ===
set nocompatible
filetype off
set rtp+=~/.vim/bundle/Vundle.vim
let path='~/.vim/bundle'
call vundle#begin(path)

Plugin 'gmarik/Vundle.vim'

Plugin 'tpope/vim-fugitive'
Plugin 'L9'
Plugin 'git://git.wincent.com/command-t.git'
Plugin 'rstacruz/sparkup', {'rtp': 'vim'}
Plugin 'The-NERD-Tree'
Plugin 'Shougo/unite.vim'
Plugin 'bling/vim-airline'
Plugin 'flazz/vim-colorschemes'
Plugin 'tomasr/molokai' 
Plugin 'terryma/vim-multiple-cursors'
Plugin 'terryma/vim-smooth-scroll'
Plugin 'Raimondi/delimitMate'
Plugin 'SirVer/ultisnips'
Plugin 'honza/vim-snippets'
Plugin 'Syntastic'
Plugin 'scrooloose/nerdcommenter'

call vundle#end()
filetype plugin indent on

" === resize windows ===
nnoremap <silent> <Leader>= :exe "resize +3"<CR>
nnoremap <silent> <Leader>- :exe "resize -3"<CR>
nnoremap <silent> <Leader>] :exe "vertical resize +8"<CR>
nnoremap <silent> <Leader>[ :exe "vertical resize -8"<CR>
 
nnoremap <silent> <Leader>+ :exe "resize " . (winheight(0) * 3/2)<CR>
nnoremap <silent> <Leader>_ :exe "resize " . (winheight(0) * 2/3)<CR>
nnoremap <silent> <Leader>} :exe "vertical resize " . (winheight(0) * 3/2)<CR>
nnoremap <silent> <Leader>{ :exe "vertical resize " . (winheight(0) * 2/3)<CR>

" === vim-multiple-cursor ===
let g:multi_cursor_use_default_mapping=0
" Default mapping
let g:multi_cursor_next_key='<C-n>'
let g:multi_cursor_prev_key='<C-p>'
let g:multi_cursor_skip_key='<C-x>'
let g:multi_cursor_quit_key='<Esc>'
 
" === vim-smooth-scroll ===
noremap <silent> <c-b> :call smooth_scroll#up(&scroll*2, 10, 5)<CR>
noremap <silent> <c-f> :call smooth_scroll#down(&scroll*2, 10, 5)<CR>
noremap <silent> <c-u> :call smooth_scroll#up(&scroll, 10, 3)<CR>
noremap <silent> <c-d> :call smooth_scroll#down(&scroll, 10, 3)<CR>

" === delimitMate ===
let delimitMate_expand_cr=1

" === UltiSnips ===
let g:UltiSnipsExpandTrigger="<tab>"
let g:UltiSnipsJumpForwardTrigger="<tab>"
let g:UltiSnipsJumpBackwardTrigger="<s-tab>"
let g:UltiSnipsEditSplit="vertical"

" === Syntastic ===
set statusline+=%#warningmsg#
set statusline+=%{SyntasticStatuslineFlag()}
set statusline+=%*

let g:syntastic_always_populate_loc_list = 1
let g:syntastic_auto_loc_list = 1
let g:syntastic_check_on_open = 1
let g:syntastic_check_on_wq = 0

let g:syntastic_cpp_compiler = 'g++'
let g:syntastic_cpp_compiler_options = "-std=c++11 -Wall -Wextra -Wpedantic"
let g:syntastic_c_compiler_options = "-std=c11 -Wall -Wextra -Wpedantic"

" === NERD Commenter ===
" Add spaces after comment delimiters by default
let g:NERDSpaceDelims = 1
" Use compact syntax for prettified multi-line comments
let g:NERDCompactSexyComs = 1
" Align line-wise comment delimiters flush left instead of following code indentation
let g:NERDDefaultAlign = 'left'
" Set a language to use its alternate delimiters by default
let g:NERDAltDelims_java = 1
" Add your own custom formats or override the defaults
let g:NERDCustomDelimiters = { 'c': { 'left': '/**','right': '*/' } }
" Allow commenting and inverting empty lines (useful when commenting a region)
let g:NERDCommentEmptyLines = 1
" Enable trimming of trailing whitespace when uncommenting
let g:NERDTrimTrailingWhitespace = 1
" customize keymapping
map <Leader>cc <plug>NERDComToggleComment
map <Leader>c<space> <plug>NERDComComment
```
.vimrc 연 상태에서
``` bash
:w
:PluginInstall
```


### Homebrew
---
``` shell
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
[Homberw HomePage](https://brew.sh/index_ko)


### ZSH and Oh-My-ZSH
---
#### zsh with brew install
``` shell
$ brew update
$ brew install zsh
```
#### install with curl
``` shell
$ sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
#### Change Shell
``` shell
$ chsh -s `which zsh`
```

#### Powerlevel10k
``` shell
$ git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```
``` shell
$ vi ~/.zshrc
```
zshrc에 추가
``` shell
ZSH_THEME="powerlevel10k/powerlevel10k"
```
``` shell
$ p10k configure
```


### Tmux
---

#### install

``` shell
$ brew install tmux
```

#### WARNING
``` shell
WARNING! Your terminal appears to support fewer than 256 colors!
If your terminal supports 256 colors, please export the appropriate environment variable
_before_ loading this theme in your ~/.zshrc. In most terminal emulators, putting
export TERM="xterm-256color" at the top of your ~/.zshrc is sufficient.
```

``` shell
$ vi .zshrc
```
추가
``` bash
export TERM="xterm-256color"
```

### Plugin
---

#### zsh-autosuggestions
```shell
$ brew install zsh-autosuggestions
```
Plugin 적용
``` bash
plugins=(
zsh-autosuggestions)
```

#### Syntax highlighting
```shell
$ brew install zsh-syntax-highlighting
```
Plugin 적용
``` bash
plugins=(
zsh-syntax-highlighting
)
```

#### autojump
```shell
$ brew install autojump
```
Plugin 적용
``` bash
plugins=(
    autojump
)
```

#### FZF
``` shell
$ brew install fzf
```
Plugin 적용
``` bash
plugins=(
   fzf
)
```

#### LSD
``` shell
$ brew install lsd
```

zsh 적용
``` shell
alias ls='lsd'
alias ll='ls -alhF'
```
