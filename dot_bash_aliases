# ~/.bash_aliases

# General
alias ll='ls -l'

# Homebrew
if type brew > /dev/null; then
    alias brew-clean-cache="if [[ $(brew --cache) == *Library* ]]; then find $(brew --cache) -name '*.tar.gz' -o -name '*.dmg' -o -name '*.pkg' | xargs rm; fi"
fi

# Emacs
alias ec='emacsclient -nw'

# Git / Hub
if type hub > /dev/null; then
    alias git=hub
fi

# Docker
# See also https://www.calazan.com/docker-cleanup-commands/

# Kill all running containers.
alias dockerkillall='docker kill $(docker ps -q)'

# Delete all stopped containers.
alias dockercleanc='printf "\n>>> Deleting stopped containers\n\n" && docker rm $(docker ps -a -q)'

# Delete all untagged images.
alias dockercleani='printf "\n>>> Deleting untagged images\n\n" && docker rmi $(docker images -q -f dangling=true)'

# Delete all stopped containers and untagged images.
alias dockerclean='dockercleanc || true && dockercleani'

