Linux file permissions use letters: `r` for read, `w` for write, and `x` for execute. They apply to the owner, group, and others. For example, `rwx-rw-r--` means the owner can read and write and execute, the group can read and write, and others can read only

____
read is 4, write is 2, and execute is 1. Combining these values gives a three-digit octal number. For example, rw-r--r-- is 644, where the owner has read and write, and the group and others have read-only permissions.
7 = rwx
5 = r-x
6 = rw-
3 = -wx
1 = --x
2 = -w-

___


>chmod go-w script.sh  = remove write and exute and read permission from group and other to the script.h



