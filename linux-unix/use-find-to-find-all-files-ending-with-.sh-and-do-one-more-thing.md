---
description: Find 找到目录下所有.sh结尾文件并ll
---

# use Find to find all files ending with .sh and do one more thing

**find . -name '\*.sh' \| xargs -n 1 ls -la**

_find . -name '\*.sh' \| xargs -n 1 chmod +x_

```text
dayuan1@linux1 dayuan1] find . -name '*.sh' | xargs -n 1 ls -la
-rwx------ 1 dayuan1 rpc 248 Jun 21 16:44 ./ack1/ex1.sh
-rwx------ 1 dayuan1 rpc 1044 Jun 21 16:44 ./ack1/ex2.sh
-rwx------ 1 dayuan1 rpc 1219 Jun 21 16:44 ./ack1/ex3.sh
-rwx------ 1 dayuan1 rpc 175 Jun 21 16:44 ./ack1/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 338 Jun 21 16:44 ./ack1/lab2b_2.sh
-rwx------ 1 dayuan1 rpc 444 Jun 21 16:44 ./ack1/lab2b_3.sh
-rwx------ 1 dayuan1 rpc 326 Jun 21 16:44 ./ahmed42/ex1.sh
-rwx------ 1 dayuan1 rpc 2019 Jun 21 16:44 ./ahmed42/ex2.sh
-rwx------ 1 dayuan1 rpc 2899 Jun 21 16:44 ./ahmed42/ex3.sh
-rwx------ 1 dayuan1 rpc 225 Jun 21 16:44 ./ahmed42/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 2451 Jun 21 16:44 ./ahmed42/lab2b_2.sh
-rwx------ 1 dayuan1 rpc 3475 Jun 21 16:44 ./ahmed42/lab2b_3.sh
-rwx------ 1 dayuan1 rpc 223 Jun 22 17:57 ./ahmed42/lab2b_1da.sh
-rwx------ 1 dayuan1 rpc 2449 Jun 22 17:58 ./ahmed42/lab2b_2da.sh
-rwx------ 1 dayuan1 rpc 3473 Jun 22 18:00 ./ahmed42/lab2b_3da.sh
-rw------- 1 dayuan1 rpc 234 Jun 21 16:44 ./pburgos1/ex1.sh
-rw------- 1 dayuan1 rpc 904 Jun 21 16:44 ./pburgos1/ex2.sh
-rw------- 1 dayuan1 rpc 1057 Jun 21 16:44 ./pburgos1/ex3.sh
-rw------- 1 dayuan1 rpc 134 Jun 21 16:44 ./pburgos1/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 1166 Jun 21 16:44 ./castlek1/lab2a_2.sh
-rwx------ 1 dayuan1 rpc 1559 Jun 21 16:44 ./castlek1/lab2a_3.sh
-rwx------ 1 dayuan1 rpc 757 Jun 21 16:44 ./castlek1/lab2a_1.sh
-rwx------ 1 dayuan1 rpc 143 Jun 21 16:44 ./castlek1/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 559 Jun 21 16:44 ./castlek1/lab2b_2.sh
-rwx------ 1 dayuan1 rpc 1414 Jun 21 16:44 ./castlek1/lab2b_3.sh


[dayuan1@linux1 dayuan1] find . -name '*.sh' | xargs -n 1 chmod +x
[dayuan1@linux1 dayuan1] find . -name '*.sh' | xargs -n 1 ls -la
-rwx------ 1 dayuan1 rpc 248 Jun 21 16:44 ./ack1/ex1.sh
-rwx------ 1 dayuan1 rpc 1044 Jun 21 16:44 ./ack1/ex2.sh
-rwx------ 1 dayuan1 rpc 1219 Jun 21 16:44 ./ack1/ex3.sh
-rwx------ 1 dayuan1 rpc 175 Jun 21 16:44 ./ack1/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 338 Jun 21 16:44 ./ack1/lab2b_2.sh
-rwx------ 1 dayuan1 rpc 444 Jun 21 16:44 ./ack1/lab2b_3.sh
-rwx------ 1 dayuan1 rpc 326 Jun 21 16:44 ./ahmed42/ex1.sh
-rwx------ 1 dayuan1 rpc 2019 Jun 21 16:44 ./ahmed42/ex2.sh
-rwx------ 1 dayuan1 rpc 2899 Jun 21 16:44 ./ahmed42/ex3.sh
-rwx------ 1 dayuan1 rpc 225 Jun 21 16:44 ./ahmed42/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 2451 Jun 21 16:44 ./ahmed42/lab2b_2.sh
-rwx------ 1 dayuan1 rpc 3475 Jun 21 16:44 ./ahmed42/lab2b_3.sh
-rwx------ 1 dayuan1 rpc 223 Jun 22 17:57 ./ahmed42/lab2b_1da.sh
-rwx------ 1 dayuan1 rpc 2449 Jun 22 17:58 ./ahmed42/lab2b_2da.sh
-rwx------ 1 dayuan1 rpc 3473 Jun 22 18:00 ./ahmed42/lab2b_3da.sh
-rwx------ 1 dayuan1 rpc 234 Jun 21 16:44 ./pburgos1/ex1.sh
-rwx------ 1 dayuan1 rpc 904 Jun 21 16:44 ./pburgos1/ex2.sh
-rwx------ 1 dayuan1 rpc 1057 Jun 21 16:44 ./pburgos1/ex3.sh
-rwx------ 1 dayuan1 rpc 134 Jun 21 16:44 ./pburgos1/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 1166 Jun 21 16:44 ./castlek1/lab2a_2.sh
-rwx------ 1 dayuan1 rpc 1559 Jun 21 16:44 ./castlek1/lab2a_3.sh
-rwx------ 1 dayuan1 rpc 757 Jun 21 16:44 ./castlek1/lab2a_1.sh
-rwx------ 1 dayuan1 rpc 143 Jun 21 16:44 ./castlek1/lab2b_1.sh
-rwx------ 1 dayuan1 rpc 559 Jun 21 16:44 ./castlek1/lab2b_2.sh
-rwx------ 1 dayuan1 rpc 1414 Jun 21 16:44 ./castlek1/lab2b_3.sh
```



