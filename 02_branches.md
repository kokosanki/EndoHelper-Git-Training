# Branches
"Branching" is diverging from the main line of commits, which enabled
commiting in parallel. Needless to say, branching is essential for
distributed team work. Git's branches are extremely lightweight, so it's
encouraged to create branches as often as needed.

The main branch is traditionally called `master` (although alternatives,
like "main" or "primary" are getting attention). It's what you get when you
create a new repository.

To check what branch you are currently at, enter `git branch`. You'll see
all the local branches, which is probably just he "master" branch. To see
the remote branches too, use `git branch -r`.

Now you probably saw "01_commits" on the list, cleverly disguised by using
the name of the previous lesson instead of a more descriptive name.
Check it out - quite literally - with `git checkout 01_commits`. You'll
notice a local branch tracking the remote one has been created.

