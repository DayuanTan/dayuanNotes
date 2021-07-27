# How connect local GitHub repo to remote repo 
(It's OK when you local and remote have different codes already)

## 本地的github repo如何和远程的repo关联

首先，远程可能已经建立了一个repo， 比如[https://github.com/DayuanTan/CrackCodeInterviewAndLeetcode.git](https://github.com/DayuanTan/CrackCodeInterviewAndLeetcode.git)

Maybe you readly have one repo like this [https://github.com/DayuanTan/CrackCodeInterviewAndLeetcode.git](https://github.com/DayuanTan/CrackCodeInterviewAndLeetcode.git)

  
然后在本地，合适的文件夹下面：（此时即使本地已有和远程不同的代码也没关系）

Then do following in your directory of your code which you want upload to that remote repo \(It's ok to have different code with remote code there\):

`$git init`

`$git remote add origin git@github.com:DayuanTan/CrackCodeInterviewAndLeetcode.git`

`$ git pull` 会提示设置。\(It will prompt to ask you do following:\)

  
`$ git pull origin master` or `$ git pull origin main`

  
就好了。此时会发现远程的代码被下载到本地，和本地的在一起。后面提交本地更改。

Now you have download your remote code to local, next you need to add your local code to commit and submit them to remote repo:

`$ git add .`  
`$ git commit -m 'updae readme’`  
`$ git push`  
`$ git push --set-upstream origin master`

  
结束。End.

