# 1.Setup

How to do our jobs efficiently and reproducibly

## 0\) Get a Laptop or Desktop

[mac 使用技巧](https://www.evernote.com/l/ABIaUQq5Y4ZPv53w8iYevcDzHmCNY3AfIhU)

## 1\) Get a Linux OS

### 1a\) docker or VM

```bash
##install and run a centos docker for the first time
docker pull centos
docker run -it --name=centos -h centos -v /Users/john/Documents/centos/:/mac centos
# docker run -it --name=container_name -h hostname -v /HOST_ABSOLUTE_DIR:/CONTAINER_ABSOLUTE_DIR image_name:tag
# simple version docker run -it centos

##add user
useradd john
passwd john
su john

###detach (pause) and attach
ctrl+p+q     # detach退出: 容器不关闭，容器内部正在运行的任务不会停止. ctrl+p+q表示按住ctrl不动，先按下p，后按下q
docker attach container_name # attach进入


###exit and delete a container
exit #inside docker as root, then exit
docker rm container_name
```

install basic software for centos

```bash
yum -y install vim
```

```bash
yum -y install man
yum -y install less
yum -y install wget

yum -y install make
yum -y install gcc gcc-c++
yum -y install gcc-gfortran

yum -y install bzip2-devel
yum -y install zlib-devel
yum -y install zip unzip

yum -y install xz-devel.x86_64
yum -y install libg2c.so.0
yum -y install readline-devel
yum -y install libXt-devel

mkdir /download
cd /download
wget -c http://www.cpan.org/src/5.0/perl-5.26.1.tar.gz
tar -xvzf perl-5.26.1.tar.gz
cd /download/perl-5.26.1
sh Configure -de
make
make install
```

You can also pull and run a ubuntu docker, then install basic software for ubuntu

`docker run -it --name=ubuntu -h ubuntu -v /Users/john/Documents/unbuntu/:/mac ubuntu`

```text
apt-get -qq update
apt-get -y install vim
...
```

More: [https://ygxing.gitbooks.io/docker/content/](https://ygxing.gitbooks.io/docker/content/)

### 1b\) ssh & login {#ssh}

* ssh/sftp -p XXX \(default: 22\)

> You can also using the following **SFTP/FTP clients** to mount the remote server to the local desktop, so you can edit the scripts with a GUI editor like Atom:
>
> * Transmit
> * Fetch \(education version\)

## 2\) Learn an Editor

### A. **Vim** -- [Learn Vim Progressively](http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/)

We also have [a brief version in Appendix]().

> Learn [vim](http://www.vim.org/) and it will be your last text editor. There isn’t any better text editor that I know of. It is hard to learn, but incredible to use.I suggest you teach yourself Vim in 4 steps:
>
> 1. **Survive**
> 2. Feel comfortable
> 3. Feel Better, Stronger, Faster
> 4. Use superpowers of vim

### B. **Atom --** [Tutorial and Tips ](https://www.evernote.com/l/ABJeb9FdBc1BC6AZSgWh4Ujc_StdcFYl-kw)

> A hackable text editor for the 21st century

## 3\) README and MD

Document your project using markdown language \(available in wiki, gitbook, github, etc\)

[https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## 4\)  Always Backup Data Files Regularly

> [Tips on 备份数据、保存中间数据 \| 数据安全](https://www.evernote.com/l/ABLaXPPQIg1FM5Kgl1AoLqLj67CR1Cv44ws)

**It's necessary to backup data regularly.** 

## 5\) More Readings and Practices

* [**相关教学视频**](http://list.youku.com/albumlist/show/id_51618375.html)：Week I. 0. Setup Part I，1.Setup Part II
* **for Beginners**  

&lt;&lt;Bioinformatics Data Skills&gt;&gt;

> 1\) How to Learn Bioinformatics

* **for Advanced Readers** 

&lt;&lt;Bioinformatics Data Skills&gt;&gt;

> 1\) How to Learn Bioinformatics  
> 2\) Setting up and Managing a Bioinformatics Projects

