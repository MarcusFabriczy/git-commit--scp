# Single/multi SCP Repository
SCP multiple files to the util and test nodes as a batch - a batch is specified by a Git commit hash.

You can also send files one at a time.
## Instructions 
Set the execute bit on the shell scripts
```
chmod +x multi-scp-commit
chmod +x single-scp
```
Set values for the following variables in both the `single-scp` and `multi-scp-commit` shell scripts:
* `UTIL_NODE`
* `WEB_NODE1`
* `WEB_NODE2`

To send files as a batch, use the command below.
```
/.git-commit-scp <ssh alias or hostname> <commit hash>
```
Example:
```
/.git-commit-scp unsw-mdl-nsdev acf041
```
To send a single file
```
/.multi-scp-commit <ssh alias or hostname> <path to file>
```
Example:
```
/.git-commit-scp unsw-mdl-nsdev course/view.php
```
**Note: The commit hash parameter is a way to conveniently group files, it does not grab older revisions of a
particular file.**
