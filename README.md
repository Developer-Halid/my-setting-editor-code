# My-setting-editorCode
My setting editor code



<h1>Setting vscode</h1>

<p>
{
    "window.zoomLevel": 2,
    "editor.fontSize": 17,
    "editor.fontFamily": "",
    "window.menuBarVisibility": "toggle",
    "editor.tabSize": 2,
    "editor.wordWrap": "on",
    "editor.minimap.enabled": false,
    "zenMode.hideTabs": false,
    "terminal.integrated.rendererType": "dom",
    "editor.formatOnSave": true,
    "flow.useNPMPackagedFlow": true,
    "javascript.validate.enable": false,
    "workbench.colorTheme": "Webstorm IntelliJ Darcula Theme"
    // "editor.renderIndentGuides": false,
}
</p>

<hr />

<h1>Setting vim</h1>

<p>
call plug#begin('~/.vim/plugged')

Plug 'scrooloose/nerdtree', { 'on':  'NERDTreeToggle' }
Plug 'Valloric/YouCompleteMe'
Plug 'airblade/vim-gitgutter'
Plug 'kien/ctrlp.vim'
Plug 'jiangmiao/auto-pairs'
Plug 'mattn/emmet-vim'
Plug 'tomasiser/vim-code-dark'

call plug#end()

let g:user_emmet_leader_key='<C-Z>'

set t_Co=256
set t_ut=
colorscheme codedark

set number
set expandtab
set tabstop=2
set shiftwidth=2
set smarttab
set smartindent

map <C-e> :NERDTreeToggle<CR>

map <silent> <C-h> :call WinMove("h")<CR>
map <silent> <C-j> :call WinMove("j")<CR>
map <silent> <C-k> :call WinMove("k")<CR>
map <silent> <C-l> :call WinMove("l")<CR>

function! WinMove(key)
  let t:curwin = winnr()
  exec "wincmd ".a:key
  if (t:curwin == winnr())
    if (match(a:key, '[jk]'))
      wincmd v
    else
      wincmd s
    endif
    exec "wincmd ".a:key
  endif
endfunction

</p>
