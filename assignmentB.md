Q1. What is git stash in simple words? When do we use it?

-->Answer
    git stash is a git command which provides temporary storage for uncommited changes allowing us to switch branches and make changes on different files without risk of losing these uncommited files. We may later bring back files from stash stack(temporary storage).

Q2. You have:

-app.js (tracked, modified)
-test.js (untracked)
-.env (ignored)

Which files are stashed by:

git stash
git stash -u
git stash -a

-->Answer
    app.js will get stashed by git stash
    test.js will get stashed by git stash -u  (for untracked)
    .env will get stashed by git stash -a (for all files including secret files)

Q3. Explain the difference between:

-git stash apply
-git stash pop

-->Answer
    git stash apply :- This brings file to working directory while keeping a copy in stash stack as well. Using  it we may paste same files at different stage or in different branches.
    git stash pop :- It too brings file to working directory but also it removes it from stash stack. We may only use it once for a particular stash or file. It is recommended to us pop command carefully.

Q4. When would you prefer apply over pop? Give one small example.

-->Answer
    You should prefer apply over pop when you just want to test your cade without removing it from stash stack. For example, you have fixed a bug on a bug/fix branch and you want to test it on main branch with mainstream code before merging your bug/fix branch then you should use apply.

Q5. What do these commands do?

-git stash drop
-git stash clear

-->Answer
    git stash drop :- This command is used when you want to delete a particular stash from stash stack.
    git stash clear :- This command is used when you want to delete all stashes from stash stock and start over from beginning.

Q6. You see this git stash list:

-stash@{0}: WIP on feature/login: ...
-stash@{1}: WIP on main: ...

a-Which is the latest stash?
b-If you run git stash pop, which one is removed?

-->Answer
    stash@{0}: WIP on feature/login is the latest commit
    The latest stash stash@{0} will be removed if I use git stash pop

Q7. Why is it good to use messages like:

--git stash push -m "WIP: login form"
instead of just git stash? 

-->Answer
    Using -m "message" while stashing files is very useful for understanding purpose when we need to bring stashed files back. If we don't use it the default git message will be given to stash which is same for all stashes between two commits.

Q8. Scenario:

-You are on feature/checkout.
-checkout.html is committed.
-checkout.css is staged.
-checkout.js is untracked.
-You must switch to main urgently.

Write the exact command(s) you will use to stash your work safely (include untracked files and a message).

-->Answer
    checkout.html is commited so no worry about it.
    git stash -m "WIP: on checkout.css"  --> To stash staged checkout.css file
    git stash -u -m "WIP: on checkout.js" --> To include untracked checkout.js file in stash
    git stash list --> Not mandatory, just to confirm stashes
    git switch main --> To switch main branch.