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

