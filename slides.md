# Advanced BASH and Tools

## On the plate for today:

* BASH Magic
* System Properties
* Piping
* Editing & File manipulation
* VIM
* Remote Tunneling
* Multishell

---

## DIUF Banana-Pi Cluster

![M1](http://www.banana-pi.org/images/bpi-images/M1/m11.jpg)<!-- .element height="50%" width="50%" -->

```
ssh unifrlogin@diufpc80
...
ssh unifrlogin@diufpc87
```

---

## BASH Magic

```
tab & ctrl-r
history
!!
```

>give a man a fish and you feed him for a day;
>teach a man to fish and you feed him for a lifetime
```
apropos "list dir"
man -k "find files"
```

---

## System Properties
```
cat /etc/issue
cat /proc/cpuinfo
free
df -h / du
ps / kill
top / htop
lsof
netstat
who
```

---

## First Hands-On

* Login randomly to a Pi s and find out everything you can.
* Who is on the same machine with you?
* What is the biggest mounted filesystem?
* Which ports are open? Is there a Webserver running?

---

## Piping

```
cat head tail (-v) | grep
sort
more / less
zip / bzip2
```

---

## Editing & File manipulation

* Which Keyboard Layout for coding.
```
scp
wget
rsync
find
```

---

## Second Hands-On

* Find the biggest file on the Pi.
* Get your favorit cat picture on the Pi. (wget)
* Copy the picture to the Pi on which your neighbor is. (scp)
* Get the picture onto your machine. (on Windows use PSCP)

---

## VIM

![xkcd](https://imgs.xkcd.com/comics/hottest_editors.png)

```
:q!
```

<small> Images from: https://blog.interlinked.org/tutorials/vim_tutorial.html </small>

---

### VIM Modes

![modes](https://blog.interlinked.org/static/images/modes.png)

---

### VIM Movement

```
h …move left
l …move right
k …move up
j …move down
```

---

### VIM Movement

![commands](https://blog.interlinked.org/static/images/commands.png)

---

### VIM Advanced

```
:!command
:%s/old/new/g
:sp file && ctrl-w w
```

---

## Remote (Tunneling)

Simple webserver:
```
wget https://tinyurl.com/nweb-c
gcc -O -DLINUX nweb.c -o nweb
```


```
nweb 8181 .
ssh -L 8080:diufpc80:8181 luggenm@diufpc80
ssh -L <localport>:<server>:<serverport> <user>@<sshserver>
```

---

## Multishell with tmux

* Long Running processes / Work environment
* Multiple Shells
```
tmux:           Start tmux
tmux ls:        Show running Session
tmux attach:    Attach to running Session
Ctrl-b c :      Create a new Window
Ctrl-b n :      Switch to next Window
Ctrl-b [0-9] :  Switch to Window #
Ctrl-b d:       Detach tmux
Ctrl-b k:       Destroy Session
```

* Collaborative Sessions
Note:  https://danielmiessler.com/study/tmux/

---
## Third Hands-On

* Open a tmux session on a Pi. Invite your neighbor too it.
* Open a text file with VIM.
* Show-off your VIM skills to each other.

---

## Recap

* BASH Magic
* System Properties
* Piping
* Editing & File manipulation
* VIM
* Remote Tunneling
* Multishell

