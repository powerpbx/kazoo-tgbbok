# Kazoo Development

* I'm a newb to git, this is where I write down the commands that are commonly used.
  * You should have already created a github account

```
[root@k9 kazoo-master]# pwd
/opt/kazoo-master

cat .git/config
[core]
        repositoryformatversion = 0
        filemode = true
        bare = false
        logallrefupdates = true
[remote "origin"]
        fetch = +refs/heads/*:refs/remotes/origin/*
        url = ssh://git@github.com/stormqloud/kazoo
[branch "master"]
        remote = origin
        merge = refs/heads/master
[remote "upstream"]
        url = https://github.com/2600hz/kazoo
        fetch = +refs/heads/*:refs/remotes/upstream/*
        

[root@k9 kazoo-master]# git status
# On branch master
# Your branch is ahead of 'origin/master' by 18 commits.
#
nothing to commit (working directory clean)

[root@k9 kazoo-master]# git fetch upstream
remote: Counting objects: 1495, done.
remote: Compressing objects: 100% (25/25), done.
remote: Total 1495 (delta 1062), reused 1055 (delta 1055), pack-reused 415
Receiving objects: 100% (1495/1495), 387.97 KiB, done.
Resolving deltas: 100% (1126/1126), completed with 176 local objects.
From https://github.com/2600hz/kazoo
   12350d9..67f936e  3.20       -> upstream/3.20
   11ca138..4d0a897  3.21       -> upstream/3.21
 + 5a9e5be...02f6812 KAZOO-3891 -> upstream/KAZOO-3891  (forced update)
 + 6980cf9...b880a88 KAZOO-3959 -> upstream/KAZOO-3959  (forced update)
   7cb5cbd..f57620c  KAZOO-4009 -> upstream/KAZOO-4009
 * [new branch]      KAZOO-4079 -> upstream/KAZOO-4079
 * [new branch]      KAZOO-4108 -> upstream/KAZOO-4108
   5c1280f..849005b  master     -> upstream/master
 * [new tag]         3.20.32    -> 3.20.32
 * [new tag]         3.21.33    -> 3.21.33
From https://github.com/2600hz/kazoo
 * [new tag]         3.21.32    -> 3.21.32
[root@k9 kazoo-master]# 
[root@k9 kazoo-master]# git merge upstream/master
Already up-to-date.


```

```
 1032  git config --global user.name "wlloyd"
 1033  git config --global user.email "wlloyd@stormqloud.ca"
 1034  git clone git@github.com:stormqloud/community-scripts.git
 1039  git remote add upstream https://github.com/community-scripts.git
 1040  git status -v
 1042  git remotes
 1043  git remote
 1044  git remote -v
 1045  git branch
 1046  git branch pgcdr
 1047  git checkout pgcdr
 1048  git pull upstream pgcdr
 1049  git remote -v
 1050  git pull upstream
 1051  git remote set-url upstream https://github.com/2600hz/community-scripts.git
 1052  git pull upstream pgcdr
 1053  git remote -v
 1054  git pull upstream
 1055  git branch
 1057  git pull upstream master
 1062  git add PostgreSQL-CDR/
 1063  git commit -m "new PostgreSQL to CDR stuff"
 1066  git add .
 1067  git commit -m "new PostgreSQL to CDR stuff"
 1068  git push origin pgsql
 1069  git push origin 
 1070  git branch
 1071  git push origin ?
 1072  git push origin master
 1073  git push origin pgcdr

```

```

[root@kz532 kazoo]# /opt/kazoo/scripts/conn-to-apps.sh 
Erlang R15B03 (erts-5.9.3.1) [source] [64-bit] [smp:4:4] [async-threads:0] [hipe] [kernel-poll:false]

Eshell V5.9.3.1  (abort with ^G)
(whistl...@kz532.onnet.su)1> l(kazoo_modb_maintenance).
{module,kazoo_modb_maintenance}
(whistl...@kz532.onnet.su)2> 


And you are OK:


root@kz532 kazoo]# /opt/kazoo/scripts/conn-to-apps.sh 
Erlang R15B03 (erts-5.9.3.1) [source] [64-bit] [smp:4:4] [async-threads:0] [hipe] [kernel-poll:false]

Eshell V5.9.3.1  (abort with ^G)
(whistl...@kz532.onnet.su)1> l(kazoo_modb_maintenance).
{module,kazoo_modb_maintenance}
(whistl...@kz532.onnet.su)2> 
BREAK: (a)bort (c)ontinue (p)roc info (i)nfo (l)oaded
       (v)ersion (k)ill (D)b-tables (d)istribution
^C[root@kz532 kazoo]sup kazoo_modb_maintenance delete_modbs 201505
deleting all MODBs equal to or older than 2015/5
archiving to /tmp/account%2F00%2Fdf%2Ff804b9b8a3696bc8bc2271cef711-201505.json
    archived 30 docs
    deleted: true
```
