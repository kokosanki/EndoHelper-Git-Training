# Commits
Commit is a "snapshot" of your repository at a given time. Thanks to
commits, you can go back to any snapshot at any time, store these snapshots
remotely (e.g. on github) etc. They are stored in an internal database,
under .git directory. Normally, one doesn't need to look there at all.

## Anatomy of a commit
Each commit consists of:
* hash - identifier, picked by git itself
* author
* date
* message
  * summary - the first line
  * empty line
  * details - any number of lines

You can see some examples using:
```bash
git log
```

You can also see each commit in one line, for more clarity:
```bash
git log --pretty=oneline --abbrev-commit
```

## What is "good commit"?
The opinions on what is "good" commit vary from person to person and from
team to team, but there are a few basic rules that are generally accepted:
* just the right size - too big commits are no good (bad for debugging, bad
  for keeping track, bad for git engine itself), but too small ones are
  no good either
* semantically a single "thing" - if you have two separate things to change,
  split them into two commits
* descriptive message - the message if all you have to inform what you did,
  use it wisely
  * short first line - first line is treated as the "summary"
  * details as needed - if the summary is not enough, provide more details
    in the rest of the message
* would be cool if it works - compiles, runs with no errors, passes tests,
  you name it. Not every commit can fulfill this criterion, but it's
  certainly desirable.

A practical example:
* move a file and modify it - better split it to two commits (if possible).
  Not only is it more readable, but git itself will handle it better
  (otherwise it can fail to realize it's the same file!)

## History side-note
Note that [git itself](https://github.com/git/git) is using git.
At the moment of writing, it contains 59910 commits,
[the first one](https://github.com/git/git/commit/e83c5163316f89bfbde7d9ab23ca2e25604af290)
(THE first git commit) dating back to April 8th 2005, authored by Linus
Torvalds. You have my warning: Linus is not nice.
