# IE-HW1-Q3

## First Paragraph
First we create `FileA.txt` and then update it. Then we push it to the main branch.

## Second Paragraph
First we create a `.env` file and then with this command we remove the file and also we remove it from history using `filter-branch` command:
```
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch .env' --prune-empty --tag-name-filter cat -- --all
```
then we `force push` it to main barnch:
```
git push origin --force --all
```

## Third and Fourth Paragraphs
We create and update `FileB.txt` and `FileC.txt` in commit `b2916ca6029088575e2b7c248d5bc773e35d2882` (`FileB and FileC added`) in a new branch called `new_branch`. 
<br>
Then we add 3 commits. in commit 1 `FileB.txt` is updated, in commit 2 `FileC.txt` is updated and in commit 3 `FileB.txt` is updated again. Then Using `cherry-pick` command I merged only commit 2 to the `main` branch:
```
git cherry-pick e456f12
```
and after that with `rebase` command other two commits are mergerd to the `main` branch:
```
git rebase new_branch
```
