# my-vimrc

```vim
"  whoxer vimrc |
"  --------------

set number
set mouse=a
set title
set cursorline

set encoding=utf-8 " Importante para o YCM

let g:ycm_global_ycm_extra_conf = '~/.vim/.ycm_extra_conf.py'
set completeopt-=preview
let g:ycm_show_diagnostics_ui = 0

map q :quit<CR>
map <C-t> :NERDTreeToggle<CR>
map <C-s> :write<CR> "echo 'stty -ixon' >> ~/.bashrc && exec $SHELL'

let g:ycm_language_server =
  \ [{
  \   'name': 'ccls',
  \   'cmdline': [ 'ccls' ],
  \   'filetypes': [ 'c', 'cpp', 'cuda', 'objc', 'objcpp' ],
  \   'project_root_files': [ '.ccls-root', 'compile_commands.json' ]
  \ }]

let g:ycm_clangd_args=['--header-insertion=never']
let g:ycm_key_list_select_completion = ['<C-n>', '<Down>']
let g:ycm_key_list_previous_completion = ['<C-p>', '<Up>']
let g:SuperTabDefaultCompletionType = '<C-n>'
let g:UltiSnipsExpandTrigger = "<tab>"
let g:UltiSnipsJumpForwardTrigger = "<tab>"
let g:UltiSnipsJumpBackwardTrigger = "<s-tab>"

call plug#begin('~/.vim/plugged')
	Plug 'vim-airline/vim-airline'
	Plug 'preservim/nerdtree'
	Plug 'tpope/vim-surround'
	Plug 'junegunn/vim-easy-align'
	Plug 'https://github.com/jiangmiao/auto-pairs.git'
	Plug 'rainglow/vim'
	Plug 'ycm-core/YouCompleteMe'
	Plug 'jiangmiao/auto-pairs'
	Plug 'SirVer/ultisnips'
	Plug 'honza/vim-snippets'
	Plug 'ervandew/supertab'
call plug#end()

```
