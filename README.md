`Note: This is an early alpha version! Please don't use it in production already. It is far from deployable. If you're interested please get in contact with me.`
# ansible-role-isynet
Ansible roles to build a mssql/samba linux-server (currently only ubuntu 16.04) with an [x.isynet](https://arztsoftware.medatixx.de/software/xisynet/) server with a backup solution (and possibly later a client) installation from scratch(optionally with a given backup).

## Dependencies

## Configuration 

## Steps restore/deploy server (executed on new linux machine)
1) Download `7zip` backup file from samba or sftp.
2) Extract `7zip` to local file.
3) Install `mssqlserver` for linux.
4) Import database backup with proper permissions.
5) Install and configure `samba`.
6) Copy files on `samba` share.

## Steps restore/deploy new master client (executed on new windows machine)
1) Create Users and install printer drivers, `7zip`.
2) Install `x.isynet` with remote server and local meddb.
3) Adapt `c:\WINACS.INI`

## Steps configure backup (executed on linux server)
See: gitlab repo TODO

## FAQ
* Why should I use it?
> Administrating a windows server can be a pain, costly and involves much black box magic. By relying only on mssql for linux as a black box we can bypass or minimize some of those problems and provide a clean, constistent, small-sized 2-way backup solution.

> Scaling up the number of running instances. 

> Easier and more consistent desaster/backup handling. 
