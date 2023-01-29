vim: se fdl=1:

  * This is my ([harriott](https://github.com/harriott)) fork of **[jgm/pandoc-templates](https://github.com/jgm/pandoc-templates)** - see therein for GPL license details.
  * General usage notes: [Templates](https://pandoc.org/MANUAL.html#templates).

# get this with GitHub CLI
    gh repo clone pandoc-templates

# merging from jgm upstream

    git remote -v                                # check remote locations
    git fetch upstream                           # grab the changed upstream
    git merge upstream/master -m 'merge message' # merges in the changes
    rg HEAD                                      # ripgrep for any conflicts
    git merge --abort                            # undo the merge

