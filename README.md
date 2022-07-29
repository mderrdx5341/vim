"Vundle start
set nocompatible
filetype off  "обязательно!

set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()


"репозитории на github
"Bundle 'tpope/vim-fugitive'
"Bundle 'rstacruz/sparkup', {'rtp': 'vim/'}
"Plugin 'xolox/vim-session'
Plugin 'gmarik/Vundle.vim'
Plugin 'scrooloose/nerdtree'
Plugin 'mattn/emmet-vim'
Plugin 'vim-scripts/Marks-Browser'
Plugin 'easymotion/vim-easymotion'
Plugin 'majutsushi/tagbar'
Plugin 'jwalton512/vim-blade'

Plugin 'othree/html5.vim'
Plugin 'hail2u/vim-css3-syntax'
Plugin 'groenewege/vim-less'
"Plugin 'skammer/vim-css-color' Плагин устарел и не поддерживается
Plugin 'ap/vim-css-color'
Plugin 'tomtom/tcomment_vim'
Plugin 'terryma/vim-multiple-cursors'
Plugin 'stephpy/vim-php-cs-fixer'
"Снипеты
Plugin 'tomtom/tlib_vim'
Plugin 'MarcWeber/vim-addon-mw-utils'
Plugin 'SirVer/ultisnips'
"Plugin 'garbas/vim-snipmate' " под мастдай
Plugin 'honza/vim-snippets'
"Табы
Plugin 'nathanaelkane/vim-indent-guides'
"Plugin 'Shougo/unite.vim'
Plugin 'scrooloose/syntastic'

"vue
Plugin 'posva/vim-vue'

"Markdown
Plugin 'godlygeek/tabular'
Plugin 'plasticboy/vim-markdown'

"Plugin 'airblade/vim-gitgutter'
"Bundle 'StanAngeloff/php.vim'
"Plugin 'xolox/vim-misc'
"Plugin 'xolox/vim-shell'
"Plugin 'Townk/vim-autoclose'
"Plugin 'othree/xml.vim'
"Plugin 'vim-scripts/PHPDoc-Script-PDocS'
Plugin 'othree/vim-autocomplpop'
"Plugin 'chrisbra/changesPlugin'
"Plugin 'shawncplus/phpcomplete.vim'
Plugin 'mhinz/vim-startify'
"Plugin 'mihaifm/vimpanel'
Plugin 'vim-scripts/Conque-Shell'
"Plugin 'joonty/vdebug.git'
Plugin 'tpope/vim-surround'
Plugin 'severin-lemaignan/vim-minimap'
Plugin 'mtscout6/vim-tagbar-css'
Plugin 'raimondi/delimitmate'
Plugin 'evidens/vim-twig'
Plugin 'tpope/vim-abolish'
Plugin 'cakebaker/scss-syntax.vim'

Plugin 'docteurklein/php-getter-setter.vim'

Plugin 'leafgarland/typescript-vim'
Plugin 'editorconfig/editorconfig-vim'

Plugin 'dhruvasagar/vim-dotoo'
Plugin 'tpope/vim-speeddating'
Plugin 'jceb/vim-orgmode'
Plugin 'ctrlpvim/ctrlp.vim'

"Шпаргалки
"Plugin 'dbeniamine/cheat.sh-vim'

"GO
Plugin 'fatih/vim-go' 

"Python
Plugin 'klen/python-mode' 
Plugin 'davidhalter/jedi-vim' 
Plugin 'mitsuhiko/vim-python-combined'

"Plugin 'wakatime/vim-wakatime'

"Plugin 'scrooloose/nerdcommenter'
"Plugin 'spf13/PIV'

"репозитории vim/scripts
"Plugin 'sessionman.vim'
"Plugin 'project.tar.gz'
Plugin 'bufexplorer.zip'
"Plugin 'cmdalias.vim'
Plugin 'L9'
Plugin 'FuzzyFinder'

Plugin 'derekwyatt/vim-scala'

Plugin 'vim-vdebug/vdebug'


Plugin 'vimplugin/project.vim'

"git репозитории (не на github)
"Bundle 'git://git.wincent.com/command-t.git'

"локальные git репозитории(если работаете над собственным плагином)
"Bundle 'file:///Users/gmarik/path/to/plugin'
call vundle#end()
filetype plugin indent on     " обязательно!
"Vundle end

set noautochdir

"Настройки экрана
set guifont=Consolas:h11
"set guifont=Monospace\ 11
"Ширина открываемого окна
set columns=125
"Высота открываемого окна
set lines=35
"Добавление номеров строк
set nu
"Цтветовая схема
color desert

"Убрать панель с кнопками и верхнее меню
set guioptions-=T
set guioptions-=m
"убрать swp
set noswapfile
" Включить подсветку невидимых символов
"set list
" Настройка подсветки невидимых символов
set listchars=tab:>-,eol:<

"Включает автолистане с открытыми 5 строками
set scrolloff=5

"показывать совпадающие скобки для HTML-тегов
"set matchpairs+=<:> 

" Формат строки состояния
set laststatus=2
"set statusline=%<%f%h%m%r\ %b\ %{&encoding}\ 0x\ \ %l,%c%V\ %P 
set statusline=%f:%c:%l\ (%p%%)\ %y%([%R%M]%)\ buf:\ #%n\ ASCII:\ [0x%B]\ [%{&fileencoding}]\ %{&encoding}


" Отключение оповещения морганием и звуком
set novisualbell
set t_vb=

" Кодировка терминала, должна совпадать с той, которая используется для вывода в терминал
set termencoding=utf-8

" возможные кодировки файлов и последовательность определения.
set fileencodings=utf8,cp1251
set encoding=utf8


"PHP отображение синтаксиса к phpDoc
" function! PhpSyntaxOverride()
"   hi! def link phpDocTags  phpDefine
"   hi! def link phpDocParam phpType
" endfunction
"
" augroup phpSyntaxOverride
"   autocmd!
"   autocmd FileType php call PhpSyntaxOverride()
" augroup END
"PHP end


"GitGutter disable
let g:gitgutter_enabled = 0

"Настройка символов в плагине airline
let g:airline_left_sep = '►'
let g:airline_right_sep = '◄'

let g:airline#extensions#tabline#enabled = 1
let g:airline_enable_syntastic=1

"Настройка отображения табов
let g:indent_guides_auto_colors = 0
autocmd VimEnter,Colorscheme * :hi IndentGuidesOdd  guibg=#474747 ctermbg=3
autocmd VimEnter,Colorscheme * :hi IndentGuidesEven guibg=#595959 ctermbg=4
" hi IndentGuidesOdd  guibg=#474747 ctermbg=3
" hi IndentGuidesEven guibg=#595959 ctermbg=4
"autocmd VimEnter,Colorscheme * :hi IndentGuidesOdd  guibg=gray30 ctermbg=3
"autocmd VimEnter,Colorscheme * :hi IndentGuidesEven guibg=gray45 ctermbg=4
au FileType * IndentGuidesEnable


"Настройка плагина TagBar
let g:tagbar_autofocus = 1
let g:tagbar_foldlevel = 0 "close tagbar folds by default
" Ширина окна
let g:tagbar_width = 30
" Показывать стрелки вместо +/-
let g:tagbar_iconchars = ['▶', '◢']
" Не сортировать
let g:tagbar_sort = 0

let g:tagbar_usearrows = 1

"------------------------------------Клавиши-------------------------------

" Настраиваем переключение раскладок клавиатуры по <C-L>
set keymap=russian-jcukenwin
" Раскладка по умолчанию - английская
set iminsert=0
set imsearch=0
" Переключение раскладок и индикация выбранной
    " в данный момент раскладки.
    " -->
        " Переключение раскладок будет производиться по <C-L>
        "
        " При английской раскладке статусная строка текущего окна будет синего
        " цвета, а при русской - красного.

        function MyKeyMapHighlight()
            if &iminsert == 0
                hi StatusLine ctermfg=Blue guifg=Blue
            else
                hi StatusLine ctermfg=Red guifg=Red
            endif
        endfunction

        " Вызываем функцию, чтобы она установила цвета при запуске Vim'a
        call MyKeyMapHighlight()

        " При изменении активного окна будет выполняться обновление
        " индикации текущей раскладки
        au WinEnter * :call MyKeyMapHighlight()

        cmap <silent> <C-L> <C-^>
        imap <silent> <C-L> <C-^>X<Esc>:call MyKeyMapHighlight()<CR>a<C-H>
        nmap <silent> <C-L> a<C-^><Esc>:call MyKeyMapHighlight()<CR>
        vmap <silent> <C-L> <Esc>a<C-^><Esc>:call MyKeyMapHighlight()<CR>gv
    " <--
	

let mapleader = "\<Space>"

"Tabular
nmap <Leader>a :Tabularize /=<CR>
vmap <Leader>a :Tabularize /=<CR>
nmap <Leader>A :Tabularize /:<CR>
vmap <Leader>A :Tabularize /:<CR>
nmap <Leader>b :FufBuffer <CR>
vmap <Leader>b :FufBuffer <CR>
nmap <Leader>f :FufFile <CR>
vmap <Leader>f :FufFile <CR>
nnoremap <F10> :set hlsearch! hlsearch?<CR>





"Настройка символов в командной строке
:cnoremap <C-E> <C-D>
:cnoremap <C-A> <Home>
:cnoremap <C-F> <Right>
:cnoremap <C-B> <Left>
:cnoremap <C-D> <Del>
:cnoremap <Esc>b <S-Left>
:cnoremap <Esc>f <S-Right>

"Дата
:nmap <F11> "=strftime('%c')<C-M>p
:imap <F11> <C-R>=strftime('%c')<C-M>
" ширина текста 
"set textwidth=170
" всегда делать активное окно максимального размера
"set noequalalways
"set winheight=9999
" отображение выполняемой команды
set showcmd 
" перенос по словам, а не по буквам
set linebreak
set dy=lastline
"Не менять корневую директорию
set acd
"Нормальная работа клавиши backspace, только для Windows
set bs=2

"Не выключать выделение после добавление табуляции
vnoremap > >gv
vnoremap < <gv
set nocompatible          " Because filetype detection doesn't work well in compatible mode
filetype plugin indent on " Turns on filetype detection, filetype plugins,
"and filetype indenting all of which add nice extra features to whatever language you're using
"filetype on
"filetype plugin on
"Включение подсветки синтаксиса
syntax enable  
let g:php_folding=2
"Включение сворачивание кода
set foldmethod=syntax
set foldlevel=20

"Настройка табуляции на 4 символа
set tabstop=4 shiftwidth=4 "expandtab

"Включение grep только для Windows
":let Grep_Path = 'C:\Program Files\GnuWin32\bin\grep.exe'

" Показывать положение курсора всё время.
set ruler 

" Поиск по набору текста (очень полезная функция)
set incsearch

" Игнорировать регистр при поиске, если в искомом выражении нет символов верхнего регистра
set smartcase

" Включаем "умные" отспупы ( например, автоотступ после {)
set smartindent

if version >= 700
	set history=64
	set undolevels=128
	set undodir=~/.vim/temp/
	set undofile
	set undolevels=1000
	set undoreload=10000
endif

nmap <C-B>b :BufExplorer<cr>
vmap <C-B>b <esc>:BufExplorer<cr>i
imap <C-B>b <esc>:BufExplorer<cr>i

nmap <C-N>n :NERDTreeToggle<cr>
vmap <C-N>n <esc>:NERDTreeToggle<cr>i
imap <C-N>n <esc>:NERDTreeToggle<cr>i

nmap <C-M>m :MarksBrowser<cr>
vmap <C-M>m <esc>:MarksBrowser<cr>i
imap <C-M>m <esc>:MarksBrowser<cr>i

nmap <C-N>t :TlistOpen<cr>:new<cr>:e .<cr>
vmap <C-N>t <esc>:TlistOpen<cr>:new<cr>:e .<cr>
imap <C-N>t <esc>:TlistOpen<cr>:new<cr>:e .<cr>

nmap <C-T>t :TagbarToggle<cr>
vmap <C-T>t <esc>:TagbarToggle<cr>i
imap <C-T>t <esc>:TagbarToggle<cr>i

nmap <C-P>p <Plug>ToggleProject<cr>
vmap <C-P>p <esc><Plug>ToggleProject<cr>
imap <C-P>p <esc><Plug>ToggleProject<cr>

""" меню с кодировками
set wildmenu
set wcm=<Tab>
menu Encoding.koi8-r :e ++enc=koi8-r ++ff=unix<CR>
menu Encoding.windows-1251 :e ++enc=cp1251 ++ff=dos<CR>
menu Encoding.cp866 :e ++enc=cp866 ++ff=dos<CR>
menu Encoding.utf-8 :e ++enc=utf8 <CR>
menu Encoding.koi8-u :e ++enc=koi8-u ++ff=unix<CR>

map <F2> :emenu Encoding.<TAB>
""" end меню с кодировками

nnoremap <Leader>w :w<CR>

" vmap <F3> "+y
"
" vmap <F4> "+p
" nmap <F4> "+p
" imap <F4> <Esc>"+p

vmap <Leader>y "+y
vmap <Leader>d "+d
nmap <Leader>p "+p
nmap <Leader>P "+P
vmap <Leader>p "+p
vmap <Leader>P "+P

" F5 - предыдущий буфер
nmap <F5> :bp<cr>
vmap <F5> <esc>:bp<cr>i
imap <F5> <esc>:bp<cr>i

" F6 - следующий буфер
nmap <F6> :bn<cr>
vmap <F6> <esc>:bn<cr>i
imap <F6> <esc>:bn<cr>i

" F7 - предыдущий таб
nmap <F7> :tabp<cr>
vmap <F7> <esc>:tabp<cr>i
imap <F7> <esc>:tabp<cr>i

" F8 - следующий таб
nmap <F8> :tabn<cr>
vmap <F8> <esc>:tabn<cr>i
imap <F8> <esc>:tabn<cr>i

" F7 - Новый таб
nmap <C-S-F7> :tabnew<cr>
vmap <C-S-F7> <esc>:tabnew<cr>i
imap <C-S-F7> <esc>:tabnew<cr>i

" F8 - Закрыть таб
nmap <C-S-F8> :tabclose<cr>
vmap <C-S-F8> <esc>:tabclose<cr>i
imap <C-S-F8> <esc>:tabclose<cr>i

" bash 
" nmap <C-S-B> :!bash<cr>
" vmap <C-S-B> <esc>:!bash<cr>i

"cscope
nmap <c-f> :cs find g <c-r>=expand("<cword>")<cr><cr>

nmap <C-W>+ <C-W>5+
nmap <C-W>- <C-W>5-
nmap <C-W>< <C-W>5<
nmap <C-W>> <C-W>5>

"au BufRead,BufNewFile jquery.*.js set ft=javascript syntax=jquery
"set runtimepath=$VIMRUNTIME,c:/Users/$USERNAME/vimfiles/after 
"source $VIMRUNTIME/after/plugin/snipMate.vim
"let g:snippets_dir="$HOME\vimfiles\snippets"

let g:user_zen_settings = {
\	'less' : {
\		'extends' : 'css',
\	},
\}
"Папка скриптов
:let $SC = '~/vimfiles/s/'
autocmd BufRead,BufNewFile *.todo set filetype=todo
autocmd BufRead,BufNewFile *.html set filetype=smarty
let g:yankring_max_element_length = 54194304 " 4M
setlocal spelllang=ru_ru,en_us
"setlocal spell spelllang=ru_ru,en_us
nnoremap <F12> :set spell! spell?<CR>

"линии на 81 и с 120 строки
let &colorcolumn="81,".join(range(120,999),",")
hi ColorColumn guibg=#3C2D27
"hi ColorColumn guibg=#6f5950
"hi ColorColumn guibg=#370000

"vim-session plugin
:let g:session_autosave = 'no'

set binary
set noendofline
set t_BE=

"Настройка экрана startify
let g:startify_list_order = [
		\ ['   These are my Sessions:'],
		\ 'sessions',
		\ ['   My most recently used files'],
		\ 'files',
		\ ['   My most recently used files in the current directory:'],
		\ 'dir',
		\ ['   These are my bookmarks:'],
		\ 'bookmarks',
		\ ]

"php getter_setter plugin
"let b:phpgetset_insertPosition = 2
"
" autocmd FileType php UltiSnipsAddFiletypes php
" let g:EditorConfig_core_mode = 'external_command'

let g:syntastic_mode_map = { 'passive_filetypes': ['python'] }

let g:pymode_python = 'python3'

let g:pymode_lint = 1
let g:pymode_lint_checker = "pyflakes,pep8"
"let g:pymode_lint_ignore="E501,W601,C0110"

"let g:syntastic_python_flake8_exec = 'python3'
"let g:syntastic_python_flake8_args = ['-m', 'flake8']

