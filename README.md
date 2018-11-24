# Configuration
This repository consists a list of customized configuration files for Mac OS and some basic command instructions.

[Vim](https://github.com/ppeyliang/Configuration#vim)

[Oh My Zsh](https://github.com/ppeyliang/Configuration#oh-my-zsh)

## Vim
This customization is referenced from [here](https://github.com/amix/vimrc).

### Procedure
To install the awesome version, run from terminal:
```
git clone --depth=1 https://github.com/amix/vimrc.git ~/.vim_runtime
sh ~/.vim_runtime/install_awesome_vimrc.sh
```

Replace the content in `~/.vimrc` with this [configuration file](https://github.com/ppeyliang/Configuration/blob/master/.vimrc).

Run `source ~/.vimrc` to activate the change.

### Instruction for Plugins
Opening recently opened files with [mru.vim](https://github.com/vim-scripts/mru.vim) plugin

command | Description
------- | -------
:MRU    | List and edit file
u       | Update the file list
o       | Open file in new window
v       | Open file in read-only mode
t       | Open file in new tab
gt      | Switch tab 


Distraction free mode using [goyo.vim](https://github.com/junegunn/goyo.vim)

command | Description
------- | -------
:Goyo   | Distraction free ON
:Goyo!  | Distraction free OFF   


Browse complex directory hierarchies with [NERD Tree](https://github.com/scrooloose/nerdtree) plugin

*Note: This configuration is setup to open a NERDTree automatically when vim starts up if no files were specified.*  

## Oh My Zsh
### Objective
* Solve the error: `zsh: conda command not found` when running conda command
* Create alias to easily lauch Jupyter Notebook

### Procedure
Open `~/.bash_profile` and copy the setting for Anaconda into `~/.zshrc`.

Insert below code into `~/.zshrc` and replace `...` with a default working directory that you would like Jupyter to open when launched.
```
# alias to launch Jupyter Notebook
alias jp="cd ~/.../ && jupyter notebook"
```

Run `source ~/.zshrc` to activate the change.

Type `jp` at terminal to launch the Jupyter Notebook.
