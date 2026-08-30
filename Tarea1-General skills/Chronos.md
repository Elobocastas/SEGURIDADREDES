### 🚩 [Chronos]

**Descripción:** ¿Cuál es el objetivo principal del reto o la vulnerabilidad a explotar?
How to automate tasks to run at intervals on linux servers?



**Solución:**  Aqui primero me conecte al server con la direccion que me dio 
`  ┌──(kali㉿kali)-[~]
└─$ ssh -p 58682 picoplayer@saturn.picoctf.net
``
- Despues  vi los archivos que habia y me puse a investigar 
`picoplayer@challenge:~$ dir
picoplayer@challenge:~$ dir
picoplayer@challenge:~$ ls
picoplayer@challenge:~$ ls
picoplayer@challenge:~$ cat .
./            ../           .bash_logout  .bashrc       .cache/       .profile      
picoplayer@challenge:~$ cat .
./            ../           .bash_logout  .bashrc       .cache/       .profile      
picoplayer@challenge:~$ cat .
cat: .: Is a directory
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Aug 29 22:21 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Aug 29 22:21 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ ls -l
total 0
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Aug 29 22:21 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Aug 29 22:21 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ las -la
-bash: las: command not found
picoplayer@challenge:~$ ls-la
-bash: ls-la: command not found
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Aug 29 22:21 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Aug 29 22:21 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ dir
picoplayer
picoplayer@challenge:/home$ cd picoplayer/
picoplayer@challenge:~$ dir
picoplayer@challenge:~$ ls -a
.  ..  .bash_logout  .bashrc  .cache  .profile
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Aug 29 22:21 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Aug 29 22:21 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ cd .
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ dir
picoplayer
picoplayer@challenge:/home$ cd picoplayer/
picoplayer@challenge:~$ dir
picoplayer@challenge:~$  cd /
picoplayer@challenge:/$ dir
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ cat 
.dockerenv  boot/       dev/        home/       lib32/      libx32/     mnt/        proc/       run/        srv/        tmp/        var/        
bin/        challenge/  etc/        lib/        lib64/      media/      opt/        root/       sbin/       sys/        usr/        
picoplayer@challenge:/$ cat challenge/
cat: challenge/: Permission denied
picoplayer@challenge:/$ cat b
bin/  boot/ 
picoplayer@challenge:/$ cat b
bin/  boot/ 
picoplayer@challenge:/$ cat b
bin/  boot/ 
picoplayer@challenge:/$ cat bin/
cat: bin/: Is a directory
picoplayer@challenge:/$ cat 
.dockerenv  boot/       dev/        home/       lib32/      libx32/     mnt/        proc/       run/        srv/        tmp/        var/        
bin/        challenge/  etc/        lib/        lib64/      media/      opt/        root/       sbin/       sys/        usr/        
picoplayer@challenge:/$ cat 
.dockerenv  boot/       dev/        home/       lib32/      libx32/     mnt/        proc/       run/        srv/        tmp/        var/        
bin/        challenge/  etc/        lib/        lib64/      media/      opt/        root/       sbin/       sys/        usr/        
picoplayer@challenge:/$ cat boot/
cat: boot/: Is a directory
picoplayer@challenge:/$ cat /dev
cat: /dev: Is a directory
picoplayer@challenge:/$ cat etc/
cat: etc/: Is a directory
picoplayer@challenge:/$ cd 
.dockerenv  boot/       dev/        home/       lib32/      libx32/     mnt/        proc/       run/        srv/        tmp/        var/        
bin/        challenge/  etc/        lib/        lib64/      media/      opt/        root/       sbin/       sys/        usr/        
picoplayer@challenge:/$ cd 
.dockerenv  boot/       dev/        home/       lib32/      libx32/     mnt/        proc/       run/        srv/        tmp/        var/        
bin/        challenge/  etc/        lib/        lib64/      media/      opt/        root/       sbin/       sys/        usr/        
picoplayer@challenge:/$ cd 
.dockerenv  boot/       dev/        home/       lib32/      libx32/     mnt/        proc/       run/        srv/        tmp/        var/        
bin/        challenge/  etc/        lib/        lib64/      media/      opt/        root/       sbin/       sys/        usr/        
picoplayer@challenge:/$ cd etc/
picoplayer@challenge:/etc$ dir
adduser.conf            cloud         debconf.conf    fstab      hostname     kernel         logrotate.d    mke2fs.conf          pam.conf   rc0.d  resolv.conf  ssh        sysctl.conf  update-motd.d
alternatives            cron.d        debian_version  gai.conf   hosts        ld.so.cache    lsb-release    modules-load.d       pam.d      rc1.d  rmt          ssl        sysctl.d     wgetrc
apt                     cron.daily    default         group      hosts.allow  ld.so.conf     machine-id     mtab                 passwd     rc2.d  security     subgid     systemd      xattr.conf
bash.bashrc             cron.hourly   deluser.conf    group-     hosts.deny   ld.so.conf.d   magic          networkd-dispatcher  passwd-    rc3.d  selinux      subgid-    terminfo     xdg
bindresvport.blacklist  cron.monthly  dhcp            gshadow    init.d       legal          magic.mime     networks             profile    rc4.d  shadow       subuid     timezone
binfmt.d                cron.weekly   dpkg            gshadow-   inputrc      libaudit.conf  mailcap        nsswitch.conf        profile.d  rc5.d  shadow-      subuid-    tmpfiles.d
ca-certificates         crontab       e2scrub.conf    gss        issue        localtime      mailcap.order  opt                  python3    rc6.d  shells       sudoers    ucf.conf
ca-certificates.conf    dbus-1        environment     host.conf  issue.net `


- Hasta que fui avanzando utilizando el cat p-ara ver el contenido de los archivos hasta dar con la bandera 
`icoplayer@challenge:/etc$ cat  c
ca-certificates/      ca-certificates.conf  cloud/                cron.d/               cron.daily/           cron.hourly/          cron.monthly/         cron.weekly/          crontab               
picoplayer@challenge:/etc$ cat  c
ca-certificates/      ca-certificates.conf  cloud/                cron.d/               cron.daily/           cron.hourly/          cron.monthly/         cron.weekly/          crontab               
picoplayer@challenge:/etc$ cat  cron
cron.d/       cron.daily/   cron.hourly/  cron.monthly/ cron.weekly/  crontab       
picoplayer@challenge:/etc$ cat  cron
cron.d/       cron.daily/   cron.hourly/  cron.monthly/ cron.weekly/  crontab       
picoplayer@challenge:/etc$ cat  cron.d/
cat: cron.d/: Is a directory
picoplayer@challenge:/etc$ cat crontab
[picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
picoplayer@challenge:/etc$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
`



`
[picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
}
