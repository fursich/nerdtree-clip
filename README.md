# nerdtree-iterm

## Introduction

The following NERDTree plugins are included:

* ```iterm_menu_item```: Adds a menu item to open the selected folder in iTerm.
  (i.e. open a shell window and cd to that folder)
* ```clip_path```: Adds a menu item to copy the selected path to the clipboard.
* ```ag_path```: Adds a menu item to search for a keyword or regex under the
  selected path using [ag.vim](https://github.com/rking/ag.vim).
* ```ags_path```: Same as ```ag_path``` but uses
  [vim-ags](https://github.com/gabesoft/vim-ags) instead.

## Installation

### Pathogen

Use the following commands:

    cd ~/.vim/bundle
    git clone https://github.com/mortonfox/nerdtree-iterm.git

### Vundle

Add the following to your vimrc:

    Plugin 'mortonfox/nerdtree-iterm'

Install with ```:PluginInstall```.

### Manual Installation

Copy the ```iterm_menu_item.vim```, ```clip_path.vim```, ```ag_path.vim```,
and ```ags_path.vim``` files to ```~/.vim/nerdtree_plugin/``` (*nix)
or ```~/vimfiles/nerdtree_plugin``` (Windows).

### iTerm2 3.x

nerdtree-iterm uses a piece of AppleScript code to open an iTerm session. This
AppleScript code is different for iTerm2 2.x and iTerm2 3.x.

By default, nerdtree-iterm supports iTerm2 2.x. If you are using iTerm2 3.x (or
an iTerm2 2.9 nightly build), add the following to your vimrc:

    let g:nerdtree_iterm_iterm_version = 3

## Usage

In the NERDTree window:

* Select the desired folder and then type ```m``` and ```i``` to open an iTerm
  session with that folder as the current directory. If the selection is on a
  file, this plugin will open iTerm on the enclosing folder.
* Select the desired folder or file and type ```m``` and ```b``` to copy its
  path to the clipboard.
* Select the desired folder and then type ```m``` and ```g```. Enter a keyword
  or regex at the prompt to get a quickfix list of ag.vim search results.
* Select the desired folder and then type ```m``` and ```s```. Enter a keyword
  or regex at the prompt to get a vim-ags search results window.
