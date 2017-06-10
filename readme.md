Workaround for plasma5 which dislikes single process multiple tray icons

Adding a -u option which skips active instance listening and checking, hence one process one window

Building:
enable deb-src http://us.archive.ubuntu.com/ubuntu/ xenial universe
(uncomment deb-src http://us.archive.ubuntu.com/ubuntu/ xenial universe in /etc/apt/sources.list then run sudo apt update, or use software sources)

$sudo apt build-dep kdocker
$cd kdocker-4.6
$dpkg-buildpackage -rfakeroot -uc -b

Note:
This particular version of kdocker builds properly with qt4, not sure about 5. Change the make file accordingly to use qmake-qt4
