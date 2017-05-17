### How to

1. Clone this   
`git clone https://github.com/1nterp/my-ultisnips.git ~/.vim/my_snippets`
2. Clone below repository    
`git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
3. Add `~/.vimrc` (see below)  
4. Install Plugin by typing `:PluginInstall` in vim


```
"""""""""""""
" Vundle
"""""""""""""
set nocompatible
filetype off
set rtp+=~/.vim/bundle/Vundle.vim

" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just
" :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to

" Begin
call vundle#begin()
Plugin 'VundleVim/Vundle.vim'

" Custom plugins below :
Plugin 'SirVer/ultisnips'           " enable snippet functionality

" End
call vundle#end()            " required
filetype plugin indent on    " required

"""""""""""""
" Vundle END
"""""""""""""

" UltiSnips
let g:UltiSnipsSnippetDirectories=["my_snippets"]
```

## More Snippets?
Please add this *vim-snippets* between `Vundle` Plugin list

```
Plugin 'honza/vim-snippets'         " various snippets for ultisnips
```

Then, you can add search directory name in `UltiSnipsSnippetDirectories`. 
Because `vim-snippets` has subdir named `UltiSnips` for various language.

```
" UltiSnips
let g:UltiSnipsSnippetDirectories=["UltiSnips", "interp_snippets"]
```
