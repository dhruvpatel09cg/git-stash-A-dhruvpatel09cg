Q1: How many stashes do you see? Which is latest (stash@{0} or stash@{1})?

-->Answer:

    I can see 2 stashes. stash@{0} is latest.

Q2: Which stash has notes.txt? How do you know?

-->Answer:

    stash@{0} has notes.txt. I know this as I have given stash message while stashing it.

Q3: What happened to the stash list after pop?

-->Answer:

    The latest stash containing notes.txt was deleted and file was present on Working Directory.

Q4: Why did you need git stash before switching to main?

-->Answer:

    We need git stash before switching to main because switching branch with uncommited files may cause
    in delete of file.

Q5: Show 1 screenshot of git stash list after pop. How many stashes remain?

-->
    After pop command only one stash left in stash.

Q6: Why is using -m "message" helpful?

-->Answer:

    Using -m "message" while stashing files is very useful for understanding purpose when we need to
    bring stashed files back. If we don't use it the default git message will be given to stash which 
    is same for all stashes between two commits.
