# chmod & chown
可以使用 `chmod` 和 `chown` 来设置文件权限。

--- 
## chmod
1. 使用 `=`

    ```sh
    chmod u=rwx g=rw o=r filename
    ```
    `u` 为用户，`g` 为用户组，`o` 为其他用户。

2. 增加减少权限

    ```sh
    chmod o+x filename
    chmod a+x filename
    chmod a-x filename
    ```
    其中 `a` 为全部。

3. 使用八进制数

    ```sh
    chmod 764 filename
    ```

    `7` 在二进制中为 `111`，也就是 `rwx`，再比如 `6`，在二进制中为 `110`，权限为 `rw-`。

## chown
1. 更改所有权

    ```sh
    chown user.group filename
    ```

2. 设置粘滞位

    ```sh
    chmod a+t directory_name
    ```

3. 以递归的形式设置权限

    ```sh
    chmod user.group . -R
    ```

4. 以不同的身份运行可执行文件（setuid）

    将文件的所有权替换为需要执行该文件的用户，然后以该用户登录。运行下面的命令：
    ```sh
    chmod +s executable_file
    ```

    当拥有该文件的用户运行这个二进制文件时，实际是以另外一个用户的身份在运行。

    > setuid 只能用于 Linux ELF 格式的二进制文件上，而不能用于脚本文件。

---

## Linux 文件系统

Linux 系统中的每一个用户都与多种类型的权限相关联。在这些权限中，我们通常要和三类权限打交道（用户、用户组和其他用户）。

**用户** 是文件的所有者。**用户组** 是多个用户的集合（由系统管理员指定），系统允许这些用户对文件进行某种形式的访问。**其它用户** 是除文件用户或用户组之外的任何人。

对于 `ls -l` 的输出结果，第 1 列代表了文件的权限，第 3 列的 `root` 代表用户，第 4 列代表用户组，对于普通文件，第 2 列代表链接数，而对于目录来说，这一列代表第一级子目录数。

```sh
-rwxrwxrwx 1 root root    27 Feb 28 09:18 B.txt
-rwxrwxrwx 1 root root    95 Feb 25 19:13 interactive.sh
-rwxrwxrwx 1 root root    42 Mar  1 19:47 in.txt
-rwxrwxrwx 1 root root   946 Feb 28 15:46 plan.md
-rwxrwxrwx 1 root root   605 Mar  1 14:09 remove_duplicates.sh
drwxrwxrwx 0 root root   512 Feb 27 14:13 winjs
```

每行第 1 个字母的含义如下：

| 字母 | 含义     |
| ---- | -------- |
| `-`  | 普通文件 |
| `d`  | 目录     |
| `c`  | 字符设备 |
| `b`  | 块设备   |
| `l`  | 符号链接 |
| `s`  | 套接字   |
| `p`  | 管道     |

剩下的部分可以分为 3 组，每组有 3 个字符，第一组的 3 个字符对应用户权限，第二组对应用户组权限，第三个对应其它用户权限。3 个字符中可能出现的字符有 `r`，`w`，`x` 分别代表读权限，写权限和执行权限。

**用户权限**的第三个字符也可以是 `S`，表示 `setuid` 权限，表示允许用户以其拥有者的权限来执行可执行文件。

对于目录来说，目录的读、写、执行权限含义是不同的。

+ 目录的读权限（r）允许读取目录中文件和子目录的列表；
+ 目录的写权限（w）允许在目录中创建或删除文件或目录；
+ 目录的执行权限（x）指明是否可以访问目录中的文件和子目录。

目录有一个特殊的权限，叫做**粘滞位（sticky bit）**。如果目录设置了粘滞位，只有创建该目录的用户才能删除目录中的文件，即使用户组和其它用户也有写权限，也无能为力。

粘滞位出现在其他用户权限中的执行位置上，如
```sh
------rwt, ------rwT
```
