# Github-Doc
Ngâm cứu Github 5/8/17
## I. Prequirement Lib
- Ubuntu/Debain
```
$ apt-get -y install libcurl4-gnutls-dev libexpat1-dev gettext \
  libz-dev libssl-dev
```
- Centos/Feroda/RHEL
```
yum -y install curl-devel expat-devel gettext-devel \
  openssl-devel zlib-devel
```
## II. Install Git
- Ubuntu/Debian
```
$ sudo apt-get install git
```
- CentOS/Fedora/RHEL
```
$ yum -y install git-core
```
## III. Active User
```
$ git config --global user.email "phihungngo249@gmail.com"
$ git config --global user.name "phihungngo"
```
- Check User Config
```
$ cat  ~/.gitconfig
[user]
        name = phihungngo
        mail = phihungngo249@gmail.com       
```        
- Check Config
```
$ git config <config-list>

Example
$ git config user.name
phihungngo

```
- Config List
```
$ git config --list
user.name=Scott Chacon
user.email=schacon@gmail.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
...
```
## IV. Create Repository
### Type I: Local Repository
- Create Repo
```
git init test-repository
Initialized empty Git repository in /home/zed/test-repository/.git/
```

- Check Status
```
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

        new file:   README
```
### Type II: Clone Repository
- Clone Repo
```
$ git clone [url] 

EX:
zed@450G1:~$ git clone https://github.com/phihungngo/Github-Doc.git
Cloning into 'Github-Doc'...
remote: Counting objects: 18, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 18 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (18/18), done.

```
- Clone Repo with new Folder
```
zed@450G1:~$ git clone https://github.com/phihungngo/Github-Doc.git new-git-doc
Cloning into 'Github-Doc'...
remote: Counting objects: 18, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 18 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (18/18), done.

```
- Add File
```
zed@450G1:~$ cd Github-Doc/
zed@450G1:~/Github-Doc$ echo "Hello Github" > HELLO.txt
zed@450G1:~/Github-Doc$ git add HELLO.txt
zed@450G1:~/Github-Doc$ git commit -m "first commit"
[master 53c47e2] first commit
 1 file changed, 1 insertion(+)
 create mode 100644 HELLO.txt
```
- Push to Github (upload file to github)
```
zed@450G1:~/Github-Doc$ git push origin master
Username for 'https://github.com': phihungngo   
Password for 'https://phihungngo@github.com': 
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 284 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/phihungngo/Github-Doc.git
   0687ef8..53c47e2  master -> master

```
- Pull to Local (update file from github to local)
```
zed@450G1:~/Github-Doc$ git pull origin master
From https://github.com/phihungngo/Github-Doc
 * branch            master     -> FETCH_HEAD
Updating 53c47e2..c3a38ed
Fast-forward
 README.md | 71 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 70 insertions(+), 1 deletion(-)

```
## V. Git Log
```
zed@450G1:~/Github-Doc$ git log -p
commit 7286093a4dfef8d2a0f5f7709beefcdb14e3b589
Author: phihungngo <phihungngo249@gmail.com>
Date:   Fri Aug 4 22:46:00 2017 +0700

    skip staging

diff --git a/testcm b/testcm
new file mode 100644
index 0000000..e69de29

commit c3a38eda4e56776496303df02e3e2fbe37d21f30
Author: phihungngo <phihungngo249@gmail.com>
Date:   Fri Aug 4 22:36:52 2017 +0700

    Update README.md

diff --git a/README.md b/README.md
index 3d994c2..2b69dec 100644
--- a/README.md
+++ b/README.md
...
```

