### Basic Command

- git init
- git remote add origin [repository address]
- git remote -v => veiw the remote address
- git add . => add all new changes
- git commit -m " " => same as save
- git push -u origin main
- git push -u --force origin main
- git pull origin (git fetch origin + git merge origin)

### Branches

1. Heard Branches : current active or checekd out branch
2. Local & Remote Branches : Mostly working branch

### Creating new branches

- git branch develop
- git branch : checking if there is any branch

```
PS C:\20205-lab\Project> git branch
  develop
* main
```

### Switch branches

- git checkout develop <br>
  => There are other function for git checkout
- git switch develop

```
PS C:\20205-lab\Project> git checkout develop
Switched to branch 'develop'
M       Climate-change
M       Corona Movie Netflex
M       Kiosk coffee JWT
```

```
PS C:\20205-lab\Project> git branch
* develop
  main
```

> After move to develop branch, making any change in the file. develop branch will only have new change.

**All this change only can be seen in develop branch**

- git add .
- git commit -m" "
- git log

```
PS C:\20205-lab\Project> git log
commit 12e7e3971efaaa081e044c1a1eeb3ea65f2a2858 (HEAD -> develop)
Author: Jinny <eui0326@gmail.com>
Date:   Wed Aug 4 22:46:10 2021 +0900

    branch

commit e6c5eb75f357a0aa2e04c970bfdb751c0cdeb32f (origin/main, main)
Author: Jinny <eui0326@gmail.com>
Date:   Wed Aug 4 22:17:12 2021 +0900

     uploaded
```

**Implement the change to master bracnh**

- git checkout master
- git merge develop => merger with master branch

```
PS C:\20205-lab\Project> git merge develop
Updating e6c5eb7..12e7e39
Fast-forward
 branch.txt => Branch test.txt | 0
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename branch.txt => Branch test.txt (100%
```

- git push

```
PS C:\20205-lab\Project> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 6 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 234 bytes | 234.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/leejineui/Projects.git
   e6c5eb7..12e7e39  main -> main

```

**All the change will be observed in repository**

### Branch remove

- git branch -d develop

```
PS C:\20205-lab\Project> git branch -d develop
Deleted branch develop (was 12e7e39).
```

**Only main branch left after deleting the develop branch**

- git branch

```
PS C:\20205-lab\Project> git branch
* main
```
