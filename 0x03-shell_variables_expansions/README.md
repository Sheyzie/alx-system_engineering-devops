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

- **file:** `1-hello_you`

---

### 2. The path to success is to take massive, determined action

- Add `/action` to the `PATH`. `/action` should be the last directory the shell looks into when looking for a program.

```plaintext
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ source ./2-path 
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/action
julien@ubuntu:/tmp/0x03$ 
```
- **file:** `2-path`

---

### 3. If the path be beautiful, let us not ask where it leads

- Create a script that counts the number of directories in the PATH.

```plaintext
julien@ubuntu:/tmp/0x03$ echo $PATH
/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
julien@ubuntu:/tmp/0x03$ . ./3-paths 
11
julien@ubuntu:/tmp/0x03$ PATH=/home/julien/bin:/home/julien/.local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:::::/hello
julien@ubuntu:/tmp/0x03$ . ./3-paths 
12
julien@ubuntu:/tmp/0x03$ 
```

- **file:** `3-paths`

---

### 4. Global variables

- Create a script that lists environment variables.

```plaintext
julien@ubuntu:/tmp/0x03$ source ./4-global_variables
CC=gcc
CDPATH=.:~:/usr/local:/usr:/
CFLAGS=-O2 -fomit-frame-pointer
COLORTERM=gnome-terminal
CXXFLAGS=-O2 -fomit-frame-pointer
DISPLAY=:0
DOMAIN=hq.garrels.be
e=
TOR=vi
FCEDIT=vi
FIGNORE=.o:~
G_BROKEN_FILENAMES=1
GDK_USE_XFT=1
GDMSESSION=Default
GNOME_DESKTOP_SESSION_ID=Default
GTK_RC_FILES=/etc/gtk/gtkrc:/nethome/franky/.gtkrc-1.2-gnome2
GWMCOLOR=darkgreen
GWMTERM=xterm
HISTFILESIZE=5000
history_control=ignoredups
HISTSIZE=2000
HOME=/nethome/franky
HOSTNAME=octarine.hq.garrels.be
INPUTRC=/etc/inputrc
IRCNAME=franky
JAVA_HOME=/usr/java/j2sdk1.4.0
LANG=en_US
LDFLAGS=-s
LD_LIBRARY_PATH=/usr/lib/mozilla:/usr/lib/mozilla/plugins
LESSCHARSET=latin1
LESS=-edfMQ
LESSOPEN=|/usr/bin/lesspipe.sh %s
LEX=flex
LOCAL_MACHINE=octarine
LOGNAME=franky
[...]
julien@ubuntu:/tmp/0x03$ 
```

- **file:** `4-global_variables`

---

### 6. Local variable

- Create a script that creates a new local variable.

    - Name: BEST
    - Value: School

- **file:** `6-create_local_variable`

---

### 7. Global variable

- Create a script that creates a new global variable.

    - Name: BEST
    - Value: School

- **file:** `7-create_global_variable`

---

### 8. Every addition to true knowledge is an addition to human power

- Write a script that prints the result of the addition of 128 with the value stored in the environment variable `TRUEKNOWLEDGE`, followed by a new line.

```plaintext
julien@production-503e7013:~$ export TRUEKNOWLEDGE=1209
julien@production-503e7013:~$ ./8-true_knowledge | cat -e
1337$
julien@production-503e7013:~$
```

- **file:** `8-true_knowledge`

---

### 9. Divide and rule

- Write a script that prints the result of `POWER` divided by `DIVIDE`, followed by a new line.

    - `POWER` and `DIVIDE` are environmental variables

 **file:** `9-divide_and_rule`
---