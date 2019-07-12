---
description: '如何在xargs中使用变量{}'
---

# how to use variable in xargs

```text
$ ls
1.txt  2.txt  3.txt  log.xml
$ ls *.txt |xargs -t -i mv {} {}.bak
mv 1.txt 1.txt.bak 
mv 2.txt 2.txt.bak 
mv 3.txt 3.txt.bak 
$ ls
1.txt.bak  2.txt.bak  3.txt.bak  log.xml
```

注意，-I 必须指定替换字符 －i 是否指定替换字符-可选 

```text
  -I R                         same as --replace=R
  -i, --replace[=R]            replace R in INITIAL-ARGS with names read
                                 from standard input; if R is unspecified,
                                 assume {}
```

```text
find . | xargs -I {} cp {} $D_PATH 
or 
find . | xargs -i cp {} $D_PATH
```

注意：cshell和tcshell中，需要将{}用单引号、双引号或反斜杠，否则不认识。bash可以不用。

In cshell and tcshell, you need to use '' or "" or \ on {}, otherwise those shell cannot recognise {}. See example below:

wrong one vs correct one: \(-t here means display the command before execuate it\)

```text

find *.pl | xargs -t -n 1 -I {} cp {} {}_dayuan.pl
cp lab3a_1.pl _dayuan.pl
cp lab3a_2.pl _dayuan.pl
cp lab3a_3.pl _dayuan.pl
cp lab3b_1.pl _dayuan.pl
cp lab3b_2.pl _dayuan.pl
cp lab3b_3.pl _dayuan.pl


find *.pl | xargs -t -n 1 -I {} cp {} '{}'_dayuan.pl

cp lab3a_1.pl lab3a_1.pl_dayuan.pl
cp lab3a_2.pl lab3a_2.pl_dayuan.pl
cp lab3a_3.pl lab3a_3.pl_dayuan.pl
cp lab3b_1.pl lab3b_1.pl_dayuan.pl
cp lab3b_2.pl lab3b_2.pl_dayuan.pl
cp lab3b_3.pl lab3b_3.pl_dayuan.pl
```



