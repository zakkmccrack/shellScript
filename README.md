# PERSONALIZED SHELL FOR ZSH

This script is an integration for the zsh shell. 
It doesn't work on bash or other shells and can create problems if you have oh-my-zsh already installed.
#### It's a project for fun
Recently i started using again linux and i wanted to change my zsh shell because my old one was too boring.

#### Feel free to suggest some change if you like to use it

# USAGE
This shell package come along with an easy personalizable shell and a CLI for UNICO api

### Abilitating the shell
Once you install the whole package, you have to add this line of code at the bottom of your -zshrc file (parsonal and root .zshrc, otherwise you'll not have this shell while on root)
```
source '{zakksh_path}'
```

Then for enabling the UNICO API CLI type these commands
```
sudo cp {unicli_file_location} /usr/local/bin/
sudo chmod 755 /usr/local/bin/unicli
```
This because '/usr/local/bin/' is the folder where every command is searched when called on shell.

Nothing more, easy peasy

### Using the shell on other folder
If you've done a fork and are messing with this script it can be more easy to run put the following command inside the  zshrc file
```
if [[ $(id -u) -eq 0 ]]; then
    source "{path_to_github_folder}/github/shellScript/.zakkzsh"
else
    source "$HOME/github/shellScript/.zakkzsh"
fi
```
In this way you can just copy if, change the path and live change the CLI without doing any other change

### If you're not using zsh as main shell
If you don't use zsh as shell and want to change you must paste the following code on your terminal
'''
sudo chsh -s /bin/zsh
sudo chsh -s /bin/zsh root
'''
so your main shell will be zsh.
