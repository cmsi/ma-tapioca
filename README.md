# tapioca

## How to build tapioca package

1. ソースファイルの準備 (ホスト上で)

        cd $HOME/vagrant/data/src
        wget https://sourceforge.net/projects/xtapp-tapioca/files/TAPIOCA173.tgz

2. ビルドディレクトリの準備

        cd $HOME/build
        sh /development/ma-tapioca/setup.sh

3. パッケージのビルド

        cd $HOME/build
        sh /development/ma-tapioca/build.sh 2>&1 | tee build.log

4. パッケージへの署名

        cd $HOME/build
        debsign tapioca_*.changes 

5. リポジトリへの登録

        cd $HOME/build
        sh /development/MateriAppsLive/repos/add_repo.sh tapioca_*.changes
