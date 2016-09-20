# git-switch
Git util that checks out branches based on grep keywords.

## How it works

Just `git switch some_string` and it will look for remote branches that contain `some_string`.

If there are more than 1 branches that return, it will tell you to give a more specific `some_string`

```bash
$ git switch 11
Too many branches match (33). Please use a more specific string.
```

__or__ give you a select-based menu to choose your branch (or cancel) if there are under 10 results.

```bash
$ git switch 111
Select a branch to switch to:
1) bug/1113/CheckingOutIsAPain
2) bug/1117/MyBranchNameIsWayTooLong
3) feature/1116/MakingCheckoutsEasy
4) Don't switch
#?
```

By default, `git switch` checks out `master`.
