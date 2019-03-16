"====================================================================
" Start vundle
"====================================================================
set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'


"====================================================================
" Write your plugins here
"====================================================================
Plugin 'Yggdroot/indentLine'
Plugin 'ntpeters/vim-better-whitespace'
Plugin 'vim-airline/vim-airline'
Plugin 'tpope/vim-fugitive'
Plugin 'majutsushi/tagbar'
Plugin 'Valloric/YouCompleteMe'


"====================================================================
" Run vundle
"====================================================================
" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line


"====================================================================
" Plugin/Tagbar Settings
"====================================================================
" Open and close the tagbar separately
nnoremap <F7> :TagbarToggle<CR>


"====================================================================
" Plugin/YouCompleteMe Settings
"====================================================================
" Instruction to compile YCMServer can be found at
"   - https://github.com/Valloric/YouCompleteMe#fedora-linux-x64
"
" $ sudo dnf install automake gcc gcc-c++ kernel-devel cmake \
"   python-devel python3-devel
" $ cd ~/.vim/bundle/YouCompleteMe && ./install.py --clang-completer

" Let YouCompleteMe know the CFLAGS for compilation
let g:ycm_global_ycm_extra_conf = '~/.vim/bundle/YouCompleteMe/.ycm_extra_conf.py'


"====================================================================
" Custom/apperance-related
"====================================================================
" colorscheme
color ron

" syntax highlight, linenum, cursorline, ruler, search-term highlight
syntax enable
set number
set cursorline
set cc=81
set hlsearch

" status line - we're using airline
let g:airline_powerline_fonts = 1
set laststatus=2

" a lightweight status line if we're not using plugin
set statusline=%F%m%r%h%w\ (%{&ff}){%Y}\ [%l,%v][%p%%]

" check & highlight tab to distinguish it from space
function! HiTabs()
    syntax match Tab /\t/
    hi Tab ctermbg=blue
endfunction
au BufEnter,BufRead * call HiTabs()
"set listchars=tab:»\ ,
set listchars=tab:\|.
set list


"====================================================================
" Custom/navigation-related
"====================================================================
" support mouse
set mouse=a
" switch across different tab
nnoremap <silent> <C-Right> :tabnext<CR>
nnoremap <silent> <C-Left> :tabprevious<CR>
nnoremap <silent> <C-t> :tabnew<CR>

" switch across different splited-screen
nnoremap <S-Down> <C-W><C-J>
nnoremap <S-Up> <C-W><C-K>
nnoremap <S-Left> <C-W><C-H>
nnoremap <S-Right> <C-W><C-L>

" search as we are typing
set incsearch

" search for current word & go to next occurance
nnoremap <silent> <C-d> :let @/=''.expand("<cword>")<cr>n

" go to next/prev matched search term and stay in the middle of screen
" nnoremap n nzz
" nnoremap N Nzz


"====================================================================
" Custom/misc
"====================================================================
" swap ; with : for convenient
nnoremap ; :
nnoremap : ;

" show all available option on screen when pressing tab
set wildmenu
set wildmode=list:longest,full

" auto-indent
set autoindent

" replace tab with space on insertion
set expandtab
set smarttab

" 4 is the perfect tab size
set tabstop=4
set softtabstop=4
set shiftwidth=4

" split screen in a way other would expected
set splitbelow
set splitright

" move line upward and downward
nnoremap <C-S-Down> :m .+1<CR>==
nnoremap <C-S-Up> :m .-2<CR>==
inoremap <C-S-Down> <Esc>:m .+1<CR>==gi
inoremap <C-S-Up> <Esc>:m .-2<CR>==gi
vnoremap <C-S-Down> :m '>+1<CR>gv=gv
vnoremap <C-S-Up> :m '<-2<CR>gv=gv

" stay in visual mode after indention
vnoremap < <gv
vnoremap > >gv

" ignore case on specific situation can be good
set ignorecase
set smartcase

" folding stuff
set foldmethod=marker

" remove all tailing whitespace in the file
autocmd BufRead,BufWrite * if ! &bin | silent! %s/\s\+$//ge | endif

" restore cursor position to where it was before
augroup JumpCursorOnEdit
   au!
   autocmd BufReadPost *
            \ if expand("<afile>:p:h") !=? $TEMP |
            \   if line("'\"") > 1 && line("'\"") <= line("$") |
            \     let JumpCursorOnEdit_foo = line("'\"") |
            \     let b:doopenfold = 1 |
            \     if (foldlevel(JumpCursorOnEdit_foo) > foldlevel(JumpCursorOnEdit_foo - 1)) |
            \        let JumpCursorOnEdit_foo = JumpCursorOnEdit_foo - 1 |
            \        let b:doopenfold = 2 |
            \     endif |
            \     exe JumpCursorOnEdit_foo |
            \   endif |
            \ endif
   " Need to postpone using "zv" until after reading the modelines.
   autocmd BufWinEnter *
            \ if exists("b:doopenfold") |
            \   exe "normal zv" |
            \   if(b:doopenfold > 1) |
            \       exe  "+".1 |
            \   endif |
            \   unlet b:doopenfold |
            \ endif
augroup END


"====================================================================
" Custom/workaround
"====================================================================
" workaround for shift+arrow to works on tmux
if &term =~ '^screen'
    " tmux will send xterm-style keys when its xterm-keys option is on
    execute "set <xUp>=\e[1;*A"
    execute "set <xDown>=\e[1;*B"
    execute "set <xRight>=\e[1;*C"
    execute "set <xLeft>=\e[1;*D"

    " tmux knows the extended mouse mode
    set ttymouse=xterm2
endif


"====================================================================
" Custom/compilation
"====================================================================
" quick compilation in vim using predefined Makefile
function! MakeAndRun()
        silent !ls Makefile>/dev/null 2>&1
                    \ || wget people.cs.nctu.edu.tw/~cyng93/Makefile
        silent make SRC=%
        redraw!
        if len(getqflist()) == 1
          !clear && ./%:r && make SRC=% clean > /dev/null
        else
          for i in getqflist()
            if i['valid']
                 cwin
                 winc p
                 return
            endif
          endfor
        endif
endfunction


function! RunHandler()
    let x = split(execute("set filetype?"), "filetype=")
    if len(x) == 1
        return
    endif

    let a:file_type = x[1]

    if a:file_type == "c"
        call MakeAndRun()
    elseif a:file_type == "python"
        !clear && ./%
    else
        echo "-- Please define RunHandler for filetype - `".a:file_type."`"
    endif
endfunction


function! MyOTAUpdater()
    let a:url = "https://people.cs.nctu.edu.tw/~cyng93"
    execute("silent !md5sum ~/.vimrc.me | awk '{print $1}' > /tmp/l.md5")
    execute("silent !curl -s ".a:url."/.vimrc.me.md5 > /tmp/r.md5")
    if strlen(system("diff /tmp/l.md5 /tmp/r.md5")) == 0
        !clear; echo '-- `vimrc` up to date'
    else
        let a:reply = input("-- `vimrc` outdated, update it? [ Y / n ] ")
        if a:reply != "n"
            let a:cmdmv = "mv ~/.vimrc.me ~/.vimrc.me.old"
            let a:cmddl = "curl -s ".a:url."/.vimrc.me > ~/.vimrc.me"
            let a:cmdall = "!clear && echo '-- Updating `vimrc`...' && "
                          \.a:cmdmv." && ".a:cmddl." && echo '-- Updated'"
            execute(a:cmdall)
        else
            !clear; echo '-- Old `vimrc` was kept'
        endif
    endif
    redraw!
endfunction


nmap <F2> ;call MyOTAUpdater()<cr>
nmap <F5> ;call RunHandler()<cr>
