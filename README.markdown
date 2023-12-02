vim: se fdl=3:

  1. this is my ([harriott](https://github.com/harriott)) fork of **[jgm/pandoc-templates](https://github.com/jgm/pandoc-templates)** - see therein for GPL license details
  1. jgm's general usage notes: [Templates](https://pandoc.org/MANUAL.html#templates)
  1. my only adaptation here is of `default.latex` for my [md4pdf/defaults.yaml](https://github.com/harriott/md4pdf/blob/master/defaults.yaml)
Grab this repository with `GitHub CLI`: `gh repo clone pandoc-templates`.

## my maintenance routine
1) `rsync -irtv --delete $onGH/pandoc-templates/ $DJH/pandoc-templates-backup`

2) in `$onGH/pandoc-templates`, get jgm `upstream` and merge:

    git remote -v                                # check remote locations
    git fetch upstream                           # grab the changed upstream
    git merge upstream/master -m 'merge message' # merges in the changes
    rg HEAD                                      # ripgrep for any conflicts
    git merge --abort                            # undo the merge

3) fix through to `defaultJH2.latex` (for `$MD4PDF/defaults.yaml`)
3a) diff `default.latex` (jgm's) against my `defaultJH0.latex`, updating the latter
3a) diff my `defaultJH0.latex` against my `defaultJH1.latex`, updating the latter
3a) diff my `defaultJH1.latex` against my `defaultJH2.latex`, updating the latter

4) `mt` to test

5) if all good, `rm -r $DJH/pandoc-templates-backup`

