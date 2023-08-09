# Git
```
$ git --version
```
## User information
```
$ git config --global [--add|--unset] user.name '[name]'
```
```
$ git config --global [--add|--unset]  user.email '[email address]'
```
* none+none:cheke
* --add:add
* --unset:delete
* none+name:modify
```
$ git config --global color.ui true
```
```
$ git config --list
```
*Viewing Configuration Information,also see ~/.gitconfig*

## Create Git Warehouse
```
$ git init [newrepo]
```
```
$ git clone <url> [directory|alias]
```
## Submission and modification
```
$ git status [-s]
```
* ？？:first creation but untracked files
* green A:files modified can be submitted to the git repository for backup processing
* red M :local files are different from staging area files
* green M:staging area files are different from previous commit version
* green D:files Backed up is not the local files
```
$ git diff [--param] [flie]
```
* none:differences between staging area and workspace
* --cached/staged:The difference between the staging area and the previous commit
* git diff [branch1] [branch2] --stat:show the differences between branch1 and branch2
* git diff [branch1] [branch2] [filepath]:Display detailed differences for the file

```
$ git add <file1> [file2]
```
* . represents all files 
```
$ git commit <file1> [file] -m '[message]'
```
* git commit -a= git add + git commit
<!-- This content will not appear in the rendered Markdown -->

```
$ git reset [--soft|--mixed|--hard] [HEAD]
```
* --mixed(default):reset the files in the staging area to be consistent with the previous commit
* --soft:fallback to a certain commit version
* --hard(caution):revoke all uncommitted modifications in the workspace, return the staging area and workspace to the previous version, and delete all previous information submissions
* HEAD(HEAD ~0) current version, HEAD^(HEAD ~1) last version, HEAD^^^（HEAD^3）last last last version

  *git reset HEAD :cancel cached content*
  
```
$ git rm [-f|--cached|-r] <file>
```
*remove file from staging and workspace*
* -f :if the deletion has been previously modified and has been placed in the staging area, the forced deletion option must be used
* --cached:remove files from the staging area
* -r :recursively delete directory
```
$ git mv [-f] <file> <newFile>
```
* -f :rename to an existing file
## Submit Log
```
$ git log [option] [branch name/submit hash]
```
* --oneline: display submission information in a concise one line format.
* --reverse:reverse display of all logs
* --graph: display branch and merge history in a graphical manner.
* --author=<Author>: only displays submissions from specific authors.
* --since=<Time>: only displays submissions after the specified time.
* --until=<Time>: only displays submissions before the specified time.
* --decorate: displays the submission pointed to by the branch and label.
* --grep=<Mode>: only display submission messages containing the specified mode.
* --no-merges: do not display merge submissions.
* --stat: display brief statistical information, including modified files and number of lines.
* --abbrev-commit: use a short commit hash value.
* --pretty=<Format>: use a custom submission information display format
* -p: display the submitted patches (specific changes).
```
$ git blame [option] <file path>
```
* -L <StartLineNumber>,<EndLineNumber>: only display code comments within the specified line number range.
* -C:for renamed or copied lines of code, also perform line tracing.
* -M:for moving code lines, also perform code line tracing.
* -C-C or -M -M:for lines of code with significant changes, further traceability is carried out.
* --show-stats: displays statistical information on the number of rows containing each author.

## Remoting
```
$ git remote [...]
```
* git remote:list the configured remote warehouses in the current warehouse.
* git remote -v:list the configured remote warehouses in the current warehouse and display their URLs.
* git remote add <remotename> <remoteurl>: add a new remote warehouse,specify the name and URL of a remote warehouse and add it to the current warehouse.HTTPS, SSH, or Git protocol link to remote Git warehouse
* git remote rename <oldname> <newname>: rename the configured remote warehouse.
* git remote remove <remotename>: delete the specified remote warehouse from the current warehouse.
* git remote set-url <remotename> <newurl>: modify the URL of the specified remote warehouse.
* git remote show <remotename>: display detailed information about the specified remote warehouse, including URLs and tracking branches.
```
$ git fetch [alias]
```
```
$ git merge [alias]/[branch]
```
```
$ git pull <Remote Host Name> <Remote Branch Name>:<Local Branch Name>
```
*git pull=git fetch + git merge*
* if the remote branch is merged with the current branch, the part after the colon can be omitted
```
$ git push <Remote Host Name> <Remote Branch Name>:<Local Branch Name>
```
* if the local branch name is the same as the remote branch name, the colon can be omitted
```
$ git remote rm [alias]
```
## Git Branch Management
```
$ git branch [-d] [branchname)
```
* none+none:list your local branches
* none+branchname:list your local branches
* -d:delete the branch
```
$ git checkout [-b] (branchname)
```
* -b:create a new branch and immediately switch to that branch
```
$ git merge
```
## Git tag
```
$ git tag [-a|-d] <tagname> [commit] -m "tagcontent"
```
* -d:delete the tag
*git tag View all tags,git log --decorate show labels*
```
$ git show <tagname>
```


















