# 0x03. Shell, init files, variables and expansions

## Requirements

- Allowed editors: vi, vim, emacs

- All your scripts will be tested on Ubuntu 20.04 LTS

- All your scripts should be exactly two lines long ($ wc -l file should print 2)

- All your files should end with a new line (why?)

- The first line of all your files should be exactly #!/bin/bash

- A README.md file, at the root of the folder of the project, describing what each script is doing

- You are not allowed to use &&, || or ;

- You are not allowed to use bc, sed or awk

- All your files must be executable

## Tasks

### 0. &lt;o&gt;

- Create a script that creates an alias.

    - Name: `ls`
    - Value: `rm *`

```plaintext
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias 
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
julien@ubuntu:/tmp/0x03$ 
```
- **file:** `0-alias`

---

### 1. Hello you

- Create a script that prints `hello user`, where user is the current Linux user.

```plaintext
julien@ubuntu:/tmp/0x03$ id
uid=1000(julien) gid=1000(julien) groups=1000(julien),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare)
julien@ubuntu:/tmp/0x03$ ./1-hello_you 
hello julien
julien@ubuntu:/tmp/0x03$ 
```

- - **file:** `1-hello_you`

---

### 2. The path to success is to take massive, determined action

- Add `/action` to the PATH. `/action` should be the last directory the shell looks into when looking for a program.

```plaintext
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ source ./2-path 
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action
julien@ubuntu:/tmp/0x03$ 
```
- - **file:** `2-path`

---

