Source obtained from deb-src http://us.archive.ubuntu.com/ubuntu/ xenial universe 

Workaround for plasma5 which dislikes single process multiple tray icons

Adding a -u option which skips active instance checking and new instance listening, hence one window one kdocker process

Building:
enable deb-src http://us.archive.ubuntu.com/ubuntu/ xenial universe
(uncomment deb-src http://us.archive.ubuntu.com/ubuntu/ xenial universe in /etc/apt/sources.list then run sudo apt update, or use software sources gui)

'''
$ sudo apt build-dep kdocker
$ cd kdocker-4.6
$ dpkg-buildpackage -rfakeroot -uc -b
'''

Note:
This particular version of kdocker builds properly with qt4, not sure about 5. Change the make file accordingly to use qmake-qt4
