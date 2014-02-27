ipynb_template
==============

Template for creating a new git repo for an ipython notebook

1. Clone this repository 
1. Rename the directory to something meaningful

1. Make sure `nbstripout` is in your path and chmod +x

1. Add the following to your .gitconfig:

    	[filter "nbstrip"]        
    	    clean = /home/cfriedline/bin/nbstriout
    		smudge =cat
    		required

1. create a new github repo and change the origin in `.git/config`
    
    	git remote set-url origin git@github.com:cfriedline/[new_repo].git
