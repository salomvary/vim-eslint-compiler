## Vim ESLint Compiler

### Installation

Install [ESLint](http://eslint.org/) (0.5.1 or later)

If you are using [pathogen](https://github.com/tpope/vim-pathogen):

```sh
cd ~/.vim/bundle
git clone https://github.com/salomvary/vim-eslint-compiler.git
```

If not, simply save [compiler/eslint.vim](compiler/eslint.vim) to your
.vim/compiler folder.

### Usage

The primary purpose of this script is to validate multiple files or folders
recursively and help fixing issues from the quickfix window.

```vim
:compiler eslint

"Validate current folder recursively:
:make .

"Validate current file:
:make %

"Validate a folder:
:make app

"Show reults in quickfix window
:copen
```

Further information:

```vim
:help compiler
:help make
:help quickfix
```

**Note**: if you rather need inline ESLint feedback while editing or never
want to check multiple files or whole projects a better option is
[Syntastic](https://github.com/scrooloose/syntastic) which has built-in ESLint
support.
