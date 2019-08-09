# 本地的github repo如何和远程的repo关联

首先，远程可能已经建立了一个repo， 

比如[https://github.com/DayuanTan/CrackCodeInterviewAndLeetcode.git](https://github.com/DayuanTan/CrackCodeInterviewAndLeetcode.git)

  
然后在本地，合适的文件夹下面：（此时即使本地已有和远程不同的代码也没关系）

`$git init`

`$git remote add origin git@github.com:DayuanTan/CrackCodeInterviewAndLeetcode.git`

`$ git pull` 会提示设置。

  
`$ git pull origin master`

  
就好了。此时会发现远程的代码被下载到本地，和本地的在一起。后面提交本地更改。

`$ git add .`  
`$ git commit -m 'updae readme’`  
`$ git push`  
`$ git push --set-upstream origin master`

  
结束。

