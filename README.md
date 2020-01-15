# Bandit: OVERTHEWIRE

##### This is a basic ctf by overthewire, wargames catagory. This writeup is userfull beginner friendly. Follow the link for extra details.

**Here is the [link](https://overthewire.org/wargames/bandit/) to ctf**

### Note:
>1. My host operating system is debian, so if you are using window install [putty](https://putty.org/) to continue but better to use any linux base os on virtualbox or any vitualization technology if you don't know follow the [link](https://youtu.be/qH8Igk2wF9o).
>2. What i will showing can be done by million other way. So open your eye while following the writeup.
>3. If you what to continue on windows machine then install [pentestbox](https://pentestbox.org/). Pentestbox is hacking tool for windows where you can run most of the command that i will showing.


#### Bandit: Level 0

![bandit level-0](https://i.imgur.com/zJMHSFJ.png)

- Open terminal 
- Read the content of the page.


#### Bandit: Level 0->1

![bandit level-0->1](https://i.imgur.com/LpCDx2S.png)

- Type command `ssh bandit.labs.overthewire.org -p 2220 -l bandit0`
- Type the password `bandit0`
- As mention the password for next level store in readme, use `cat readme`
- Copy the password `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`
- Type `exit`

**SSH more info: [link1](https://youtu.be/qWKK_PNHnnA), [link2](https://youtu.be/hQWRp-FdTpc)**

**cat more info: [link1](https://linuxize.com/post/linux-cat-command/)**


#### Bandit: Level 1->2

![bandit level-1->2](https://i.imgur.com/WXRVSFp.png)

- Type command `ssh bandit.labs.overthewire.org -p 2220 -l bandit1`
- Type the password `boJ9jbbUNNfktd78OOpsqOltutMc3MY1`
- To read - file. Type command `cat ./-`
- Copy the password `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
- Then type `exit`


#### Bandit: Level 2->3

![bandit level-2->3](https://i.imgur.com/f3wlJ5p.png)

- Type command `ssh bandit.labs.overthewire.org -p 2220 -l bandit2`
- Type the password `CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9`
- To read type `cat 'spaces in this filename'`
- Copy the password `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`
- Then type `exit`


#### Bandit: Level-3->4

![bandit level-3->4](https://i.imgur.com/g0G20io.png)

- Type command `ssh bandit.labs.overthewire.org -p 2220 -l bandit3`
- Type the password `UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK`
- Type `cd inhere` to enter inhere directory and then type `ls -a` to check for hidden file.
- Type `cat .hidden`
- Copy the password `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`
- Then type `exit`


#### Bandit: Level-4->5

![bandit level4->5](https://i.imgur.com/OkrllKP.png)

- Type command `ssh bandit.labs.overthewire.org -p 2220 -l bandit4`
- Type the password `pIwrPrtPN36QITSp3EQaw936yaFoFgAB`
- Type `cd inhere` to enter inhere directory and then type `ls` to check for files or directorys.
- Type `cat ./*`
- Copy the password `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`
- Then type `exit`


#### Bandit: Level-5->6

![bandit level4->5](https://i.imgur.com/02VHSoW.png)

- Type command `ssh bandit.labs.overthewire.org -p 2220 -l bandit5`
- Type the password `koReBOKuIDDepwhWk7jZC0RTdopnAYKh`
- Type `cd inhere` to enter inhere directory and then type `ls` to check for files or directory.
- So hints are given that file will be 'human-readable,
1033 bytes in size,
not executable'
- Using `find` command we findout the right file
- `find . -type f -size 1033c -exec cat {} \;` is collective command to find it practically.
- Copy the password `DXjZPULLxYr17uwoI01bNLQbtFemEgo7`
- Then type `exit`

**Find more info: ![link1](http://man7.org/linux/man-pages/man1/find.1.html)**