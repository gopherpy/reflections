git - bash setup
On linux command line to make command prompt provide repository details, we need to setup bash with below scripts.

user (master #) reflections#
UserName Branch	    Repository.

Download files git-completion.bash, git-prompt.sh and paste below script in .bash_profile in linux.

#Enable tab completion
source ~/git-completion.bash

# colors!
green="\[\033[0;32m\]" \n
blue="\[\033[0;34m\]" \n
purple="\[\033[0;35m\]"
reset="\[\033[0m\]"

# Change command prompt
source ~/git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
export PS1="$purple\u$green\$(__git_ps1)$blue \W $ $reset"
