Local Portfiles for MacPorts
============================

Contents 内容
------------

### py26-ecell

* science/py26-ecell

* E-Cell3 for Mac OS X 10.6 or earlier.

### py27-ecell

* science/py27-ecell

* E-Cell3 for OS X 10.7.


Usage 使い方
-----------

### 初期設定

* レポジトリのクローンを ~/github/ に作成した場合

* Portindexファイルを作成する

    cd ~/github/Portfiles
    portindex

* MacPortsの設定ファイルPortfilesのクローンを登録する

    sudo chmod +w /opt/local/etc/macports/sources.conf
    sudo emacs /opt/local/etc/macports/sources.conf

* MacPortsサーバのURLの前に、ローカルのURLを加えて保存する

    \# To get the ports tree from the master MacPorts server in California, USA use:
    \#   rsync://rsync.macports.org/release/ports/
    \# To get it from the mirror in Trondheim, Norway use:
    \#   rsync://trd.no.rsync.macports.org/release/ports/
    \# A urrent list of mirrors is available at http://trac.macports.org/wiki/Mirrors
    file:///Users/foo/github/Portfiles/
    rsync://rsync.macports.org/release/ports/ [default]

* 設定ファイルの書き込み権限を戻し、MacPortsをselfupdateする

    sudo chmod -w /opt/local/etc/macports/sources.conf
    sudo port -v selfupdate

### ポートのインストール

* E-Cell3 for Mac OS X 10.6 or earlier.

    sudo port install py26-ecell

* E-Cell3 for Mac OS X 10.7

    sudo port install py27-ecell

### ポートの更新

* Portfilesの内容が更新された際に、インストール済みのポートを更新するには：

    sudo port selfupdate
    sudo port upgrade {port name}
