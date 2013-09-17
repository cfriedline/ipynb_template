#!/usr/bin/env python
"""strip outputs from an IPython Notebook

Opens a notebook, strips its output, and writes the outputless version to the original file.

Useful mainly as a git pre-commit hook for users who don't want to track output in VCS.

This does mostly the same thing as the `Clear All Output` command in the notebook UI.

Adapted from rom https://gist.github.com/minrk/6176788 to work with
git filter driver
"""
import sys

from IPython.nbformat import current

def strip_output(nb):
    """strip the outputs from a notebook object"""
    for cell in nb.worksheets[0].cells:
        if 'outputs' in cell:
            cell['outputs'] = []
        if 'prompt_number' in cell:
            cell['prompt_number'] = ""
    return nb

if __name__ == '__main__':
    nb = current.read(sys.stdin, 'json')
    nb = strip_output(nb)
    current.write(nb, sys.stdout, 'json')

