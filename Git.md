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
* ？？:First creation but untracked files
* green A:Files modified can be submitted to the git repository for backup processing
* red M :Local files are different from staging area files
* green M:Local files are the same as staging area files
* green D:files Backed up is not the local files
```
$ git diff [--param] [flie]
```
* none:differences between staging area and workspace
* cached/staged:The difference between the staging area and the previous commit
* git diff [first-branch]...[second-branch]:differences between two submissions
```
$ git add <file1> [file2]
```
* . represents all files 
```
$ git commit <file1> [file2] -m '[message]'
```
* git commit -a= git add + git commit

```
$ git reset [--soft | --mixed | --hard] [HEAD]
```
* mixed(default):Reset the files in the staging area to be consistent with the previous commit an
* soft:Fallback to a certain version
* hard(caution):Revoke all uncommitted modifications in the workspace, return the staging area and workspace to the previous version, and delete all previous information submissions
* HEAD(HEAD\~0) current version, HEAD^(HEAD\~1) last version, HEAD^^^（HEAD^3）last last last version

  *git reset HEAD :cancel cached content*
  
```
$ git rm [-f | --cached | -r] <file>
```
*Remove file from staging and workspace*
* -f :If the deletion has been previously modified and has been placed in the staging area, the forced deletion option must be used
* --cached:Remove files from the staging area
* -r :Recursively delete directory
```
$ git mv [-f] <file> <newFile>
```
* -f :Rename to an existing file
## Submit Log
```
$ git log [option] [branch name/submit hash]
```
* --oneline: Display submission information in a concise one line format.
* --reverse:Reverse display of all logs
* --graph: Display branch and merge history in a graphical manner.
* --author=<Author>: Only displays submissions from specific authors.
* --since=<Time>: Only displays submissions after the specified time.
* --until=<Time>: Only displays submissions before the specified time.
* --decorate: Displays the submission pointed to by the branch and label.
* --grep=<Mode>: Only display submission messages containing the specified mode.
* --no-merges: Do not display merge submissions.
* --stat: Display brief statistical information, including modified files and number of lines.
* --abbrev-commit: Use a short commit hash value.
* --pretty=<Format>: Use a custom submission information display format
* -p: Display the submitted patches (specific changes).
```
$ git blame [option] <file path>
```
* -L<Start Line Number>,<End Line Number>: Only display code comments within the specified line number range.
* -C: For renamed or copied lines of code, also perform line tracing.
* -M: For moving code lines, also perform code line tracing.
* -C-C or -M -M: For lines of code with significant changes, further traceability is carried out.
* --show-stats: displays statistical information on the number of rows containing each author.

## Remoting
```
$ git remote [...]
```
* git remote: List the configured remote warehouses in the current warehouse.
* git remote - v: List the configured remote warehouses in the current warehouse and display their URLs.
* git remote add <remote_ name> <remote_url>: Add a new remote warehouse. Specify the name and URL of a remote warehouse and add it to the current warehouse.HTTPS, SSH, or Git protocol link to remote Git warehouse
* git remote rename <old_ name> <new_ name>: Rename the configured remote warehouse.
* git remote remove <remote_ name>: Delete the specified remote warehouse from the current warehouse.
* git remote set-url <remote_ name> <new_ url>: Modify the URL of the specified remote warehouse.
* git remote show <remote_ name>: Display detailed information about the specified remote warehouse, including URLs and tracking branches.
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
* If the remote branch is merged with the current branch, the part after the colon can be omitted
```
$ git push <Remote Host Name> <Remote Branch Name>:<Local Branch Name>
```
* If the local branch name is the same as the remote branch name, the colon can be omitted
```
$ git remote rm [alias]
```
## Git Branch Management
```
$ git branch [-d] (branchname)
```
* none:List your local branches
* -d:Delete the branch
```
$ git checkout [-b] (branchname)
```
* -b:Create a new branch and immediately switch to that branch
```
$ git merge
```
## Git tag
```
$ git tag [-a | -d] <tagname> [commit] -m "tagcontent"
```
* -d:delete the tag
*git tag View all tags,git log --decorate show labels*
```
$ git show <tagname>
```


















