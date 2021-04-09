# Commands used for git

## Log

- `git log --all --decorate --oneline --graph` this will show a good looking tree

## Merging

### Merge a not directly linked branch

- `git merge auth` Merge by the recursive strategy. This is used when a branch is not directly linked to the main branch (they were modifies since the branch ocurred)
 ```bash
 |\    "<- Here, use this command"
 | |
 ...
 ```
 
### Merge a not directly linked branch with conflicts

- `git merge <branch>` This will try to merge and throw an error
- `git status` Will whow the status of the current merging
- Edit the unmerged files
- You will see the next kind of information :
```
<<<<<<< HEAD          "git marker"
lorem                 "changes"
=======               "git marker"
imposum               "changes"
>>>>>>> <branch>      "git marker"
```
- To choose one modification over an other, just delete the git markers and the unwanted changes. Save
- Add the modified files with `git add`
- Do a commit
 
