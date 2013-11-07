ipynb_template
==============

Template for creating a new git repo for an ipython notebook

Copy the nbstripout to somewhere in your path and chmod +x

make sure that .gitconfig looks something like this:
    
    [filter "nbstrip"]
        clean = "/home/cfriedline/bin/nbstripout"

create a new github repo and change the origin
    
    git remote set-url origin git@github.com:cfriedline/[new_repo].git
