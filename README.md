# go-vim-install
Easy environment setup for Vim addicts and go developers on Mac OSX.

Thanks to [xlucas](https://github.com/xlucas), this is a version that modify from xlucas's [go-vim-install](https://github.com/xlucas/go-vim-install)

I like to use [gvm](https://github.com/moovweb/gvm) to instal and manage golang env, so I remove `-go` option and `-work` option only fetch the requirement tools

## Prerequire

- Xcode. Install it either from your Mac OS X install media or better, go download the latest version from http://developer.apple.com/TOOLS/Xcode/
- HomeBrew. 
- XQuartz. go download from http://xquartz.macosforge.org/landing/  

## Install

Hereinafter are two easy ways to get your vim environment ready for go development.

###### Standard

```
wget https://raw.githubusercontent.com/xlucas/go-vim-install/master/install.sh
chmod +x install.sh
```

## Usage

While there are a lot of great plugins of all kinds for Vim made by amazing people, that's always a hassle to retrieve them all, configure your `.vimrc`, install colorschemes and extra stuff to get everything eventually working. This little installer for ubuntu make the life simpler for go development with Vim, by providing a command line with 3 options to either :
- Download and install go from a remote tarball containing the go version of your choice (option `-go`).
- Setup a fully working Vim environment with amazing plugins, third party helpers and colorschemes (option `-vim`).
- Setup your go workspace with required go tools for Vim plugins (option `-work`).

Examples :

- `./install.sh -vim`
- `./install.sh -work`

Be aware to run `. ~/.profile` after a step is done so environment variables are up to date.

That's all !

## Vim environment

The script will install [pathogen](https://github.com/tpope/vim-pathogen) and the following plugins :

- [vim-go](https://github.com/fatih/vim-go)
- [YouCompleteMe](https://github.com/Valloric/YouCompleteMe)
- [tagbar](https://github.com/majutsushi/tagbar)
- [fugitive](https://github.com/tpope/vim-fugitive)
- [vim-airline](https://github.com/bling/vim-airline)
- [powerline](https://github.com/powerline/powerline)
- [NERDTree](https://github.com/scrooloose/nerdtree)
- [vim-NERDTree-tabs](https://github.com/jistr/vim-nerdtree-tabs)
- [syntastic](https://github.com/scrooloose/syntastic)
- [better-whitespace](https://github.com/ntpeters/vim-better-whitespace)
- [gundo.vim](https://github.com/sjl/gundo.vim)
- [emmet-vim](https://github.com/mattn/emmet-vim)
- [delimitMate](https://github.com/Raimondi/delimitMate)
- [vim-maximizer](https://github.com/szw/vim-maximizer)
- [tabular](https://github.com/godlygeek/tabular)
- [ultisnips](https://github.com/sirver/ultisnips)
- [vim-instant-markdown](https://github.com/suan/vim-instant-markdown)

The colorscheme bundled is a variant of [molokai](https://github.com/fatih/molokai).

Here's a screenshot of what the environment will look like :

![go-vim-install](https://raw.githubusercontent.com/xlucas/go-vim-install/master/screenshot.png)

The script will install the Monaco font. Set it with a size between 11 and 12 in your terminal configuration.

## Workspace setup

The script will install these packages in your workspace :
- [gocov](https://github.com/axw/gocov)
- [gotags](https://github.com/jstemmer/gotags)
- [gocode](https://github.com/nsf/gocode)
- [godef](https://github.com/rogpeppe/godef)
- [goimports](https://golang.org/x/tools/cmd/goimports)
- [oracle](https://golang.org/x/tools/cmd/oracle)
- [gorename](https://golang.org/x/tools/cmd/gorename)
- [golint](https://github.com/golang/lint)
- [errcheck](https://github.com/kisielk/errcheck)

Most of them are required to have the go-vim plugin fully working. Then you can run crazy things from Vim, like test units with (`:GoTest`), coverage report with (`:GoCoverage`), refactor an element name and its references (`:GoRename`), do code inspection and error checking (`:GoDoc`, `:GoInfo`, `:GoCallers`, `:GoCallees`, `:GoErrCheck` ...), build your packages (`:GoBuild`), detect unchecked errors (`:GoErrCheck`) and much more. Obviously, you can also remap all these actions to shortcuts of your choice in your `.vimrc` ! Check the go-vim plugin documentation to get [a full list](https://github.com/fatih/vim-go/blob/master/doc/vim-go.txt) of Go-specific features.

If you don't know what other plugins are doing, you will find some other tasty functionnalities in related documentations !

## Shortcuts

The following default shortcuts are set in the `.vimrc` file :

- <kbd>F2</kbd> : Create a new tab
- <kbd>F3</kbd> : Maximize/restore current window
- <kbd>F4</kbd> : Enable search highlight
- <kbd>F5</kbd> : Disable search highlight
- <kbd>F6</kbd> : Show/hide the file tree
- <kbd>F7</kbd> : Show/hide the undo tree
- <kbd>F8</kbd> : Show/hide the tagbar (shown by default)
- <kbd>F9</kbd> : Close the current tab
- <kbd>F10</kbd> : Align text using ',' as a delimiter
- <kbd>F12</kbd> : Align text using space as a delimiter
- <kbd>CTRL</kbd> + <kbd>Up</kbd> : Go to the next tab
- <kbd>CTRL</kbd> + <kbd>Down</kbd> : Go to the previous tab
- <kbd>CTRL</kbd> + <kbd>C</kbd> + <kbd>,</kbd> : Format Zen Coding
- <kbd>CTRL</kbd> + <kbd>_</kbd> : Autoclose xml/html tag(s) (repeat to close several ones)
- <kbd>CTRL</kbd> + <kbd>j</kbd> : Expand snippet
- <kbd>CTRL</kbd> + <kbd>n</kbd> : Go to next snippet item 
- <kbd>CTRL</kbd> + <kbd>p</kbd> : Go to previous snippet item
