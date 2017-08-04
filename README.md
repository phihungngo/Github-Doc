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
$ git config --global user.name "phihungngo"
$ git config --global user.email "phihungngo249@gmail.com"
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
