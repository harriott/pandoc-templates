vim: se fdl=2:

  1. this is my ([harriott](https://github.com/harriott)) fork of **[jgm/pandoc-templates](https://github.com/jgm/pandoc-templates)** - see therein for GPL license details
  1. jgm's general usage notes: [Templates](https://pandoc.org/MANUAL.html#templates)
  1. only adaptation here is of `default.latex` for my [md4pdf/defaults.yaml](https://github.com/harriott/md4pdf/blob/master/defaults.yaml)
  1. get this repository with `GitHub CLI`: `gh repo clone pandoc-templates`

## merging from jgm upstream

    git remote -v                                # check remote locations
    git fetch upstream                           # grab the changed upstream
    git merge upstream/master -m 'merge message' # merges in the changes
    rg HEAD                                      # ripgrep for any conflicts
    git merge --abort                            # undo the merge

