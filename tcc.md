#<center>tiny-c-compiler</center>

<span id="jump"></span>

[TOC]

##一、从 git 获取源码(http://repo.or.cz/tinycc.git/bundles)

Downloadable Git bundle information for project [tinycc](http://repo.or.cz/tinycc.git) as of 2018-02-03 05:56:31 UTC:

| Project                                | Bundle                                   | Size    | Expires | Behind  |
| -------------------------------------- | ---------------------------------------- | ------- | ------- | ------- |
| [tinycc](http://repo.or.cz/tinycc.git) | [tinycc-d3ecfd20.bundle](http://repo.or.cz/tinycc.git/tinycc-d3ecfd20.bundle)<br />[tinycc-d3ecfd20.bundle](./2018-02/tinycc-d3ecfd20.bundle) | 3.4 MiB | 5 days  | current |

### Instructions

#### 0. Quick Overview

1. Download the bundle (possibly resuming the download if interrupted) using any available technique.
2. Create a repository from the bundle.
3. Reset the repository’s origin to a fetch URL.
4. Fetch the latest changes and (optionally) the current HEAD symbolic ref.
5. Select a desired branch and check it out.

#### 1. Download the Bundle

Download the [tinycc-d3ecfd20.bundle](http://repo.or.cz/tinycc.git/tinycc-d3ecfd20.bundle) file using your favorite method.

Web browsers typically provide one-click pause and resume. The `curl` command line utility has a `--continue-at` option that can be used to resume an interrupted download.

*Please note that it may not be possible to resume an interrupted download after the “Expires” time shown above so plan the bundle download accordingly.*

Subsequent instructions will assume the downloaded bundle `tinycc-d3ecfd20.bundle` is available in the current directory – adjust them if that’s not the case.

#### 2. Create a Repository from the Bundle

It is possible to use the `git clone` command to create a repository from a bundle file all in one step. However, that can result in unwanted local tracking branches being created, so we do not use `git clone` in this example.

This example creates a Git repository named “`tinycc`” in the current directory, but that may be adjusted as desired:

```
git init tinycc
cd tinycc
git remote add origin ../tinycc-d3ecfd20.bundle
git fetch

```

#### 3. Reset the Origin

Assuming the current directory is still set to the newly created “`tinycc`” repository, we set the origin to a suitable fetch URL. Any valid fetch URL for the repository may be used instead of the one shown here:

```
git remote set-url origin http://repo.or.cz/tinycc.git
```

Note that the tinycc-d3ecfd20.bundle file is now no longer needed and may be kept or discarded as desired.

#### 4. Fetch Updates

Assuming the current directory is still set to the newly created “`tinycc`” repository, this example fetches the current `HEAD` symbolic ref (i.e. the branch that would be checked out by default if the repository had been cloned directly from a fetch URL instead of a bundle) and any changes made to the repository since the bundle was created:

```
git fetch --prune origin
git remote set-head origin --auto
```

The amount retrieved by the `fetch` command depends on how many changes have been pushed to the repository since the bundle was created.

The `set-head` command will be very fast and may be omitted if one’s not interested in the repository’s default branch.

#### 5. Checkout

Assuming the current directory is still set to the newly created “`tinycc`” repository, the list of available branches to checkout may be shown like so:

```shell
# git branch -r
$ git branch -r
  origin/HEAD -> origin/mob
  origin/master
  origin/mob
  origin/mob-stuff
  origin/tcc-xref
```

Note that if the repository has a default branch it will be shown in the listing preceded by “`origin/HEAD -> `”.

In this case, however, the default branch is most likely “`mob`” and may be checked out like so:

```shell
# git checkout mob
$ git checkout mob
Already on 'mob'
Your branch is up-to-date with 'origin/mob'.
```

Note that the leading “`origin/`” was omitted from the branch name given to the `git checkout` command so that the automagic DWIM (Do What I Mean) logic kicks in.

The repository is now ready to be used just the same as though it had been cloned directly from a fetch URL.

## 二、从官网获取源码包，很小，只有620多K，但是为何家中无法下载

> ### http://download.savannah.gnu.org/releases/tinycc/
>
> ```shell
> Index of /releases/tinycc/
>
> File Name  ↓ 	File Size  ↓ 	Date  ↓ 
> Parent directory/	-	-
> tcc-0.9.24-win32-bin.zip	274K	31-Mar-2008 20:54
> tcc-0.9.24.tar.bz2	356K	31-Mar-2008 20:52
> tcc-0.9.25-win32-bin.zip	280K	18-May-2009 13:14
> tcc-0.9.25.tar.bz2	374K	18-May-2009 13:27
> tcc-0.9.26-win32-bin.zip	386K	15-Feb-2013 15:22
> tcc-0.9.26-win64-bin.zip	389K	15-Feb-2013 15:24
> tcc-0.9.26.tar.bz2	514K	15-Feb-2013 15:11
> tcc-0.9.26.tar.bz2.checksums	158	16-Feb-2013 10:46
> tcc-0.9.26.tar.bz2.sig	543	16-Feb-2013 10:45
> tcc-0.9.27-win32-bin.zip	472K	17-Dec-2017 08:27
> tcc-0.9.27-win64-bin.zip	478K	17-Dec-2017 08:27
> tcc-0.9.27.tar.bz2	620K	17-Dec-2017 08:27
> Downloads will redirect to your
> ```
>
> 



## 三、神人网站

> ### https://bellard.org



## 四、具体应用实践


