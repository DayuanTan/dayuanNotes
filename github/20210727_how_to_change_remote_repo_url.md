# How to change your remote repo url/name on local 

## Scenario:

Maybe after you have been working in a repo for a while, but you changed the repo name on Github website (remote repo). 

At this moment if you continue git push on local it will tell you that the remote is not found.

It would be worse if you create a new repo remotely using the old name. This happens. 


## Example:

For exmaple you have old repo: https://github.com/DayuanTan/someproject.git. 

Then you changed it to https://github.com/DayuanTan/someproject-dev.git to keep it private. 

And then you create a new repo using the old name (https://github.com/DayuanTan/someproject.git) to set it public.


## Solution:

You need to change the remote repo url on local:

Firstly, check the git configuration:
```
$ git remote -v
origin	https://github.com/DayuanTan/someproject.git (fetch)
origin	https://github.com/DayuanTan/someproject.git (push)
```

Secondly, change the remote repo url on local:
```
$ git remote set-url origin https://github.com/DayuanTan/someproject-dev.git
$ git remote -v
origin	https://github.com/DayuanTan/someproject-dev.git (fetch)
origin	https://github.com/DayuanTan/someproject-dev.git (push)
```
