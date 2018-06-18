# ma-tapioca

## How to prepare source files for tapioca package

1. ソースファイルの準備 (ホスト上で)

        VERSION=1.7.3
        VERSION_TGZ=173
        cd $HOME/vagrant/data/src
        rm -rf TAPIOCA$VERSION_TGZ tapioca_$VERSION
        wget -O TAPIOCA$VERSION_TGZ.tgz https://sourceforge.net/projects/xtapp-tapioca/files/TAPIOCA$VERSION_TGZ.tgz/download
        tar zxvf TAPIOCA$VERSION_TGZ.tgz
        mv -f TAPIOCA$VERSION_TGZ tapioca_$VERSION
        tar zcvf tapioca_$VERSION.orig.tar.gz tapioca_$VERSION
        rm -rf TAPIOCA$VERSION_TGZ.tgz tapioca_$VERSION
