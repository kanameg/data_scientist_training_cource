# コンテナでのKaggle開発環境

このプロジェクトはVisual Studio Codeを使ってクリーンなPython環境で
Kaggleのデータ分析を行うための環境一式です。

## インストール済環境
### Python
以下のバージョンのPythonがコンテナにインストール済です。
```
Python 3.9.6
```

### ライブラリ
以下のライブラリがコンテナにインストール済です。
```
kaggle == 1.5.12
matplotlib == 3.4.2
numpy == 1.20.3
seaborn == 0.11.1
scipy == 1.6.3
jupyterlab == 3.0.16
```

## 起動方法
1. コマンド入力を開き、Remote-Containers:Reopen in Containerコマンドを起動する。  
2. コンテナが起動しコンテナ内に起動したシェルがオープンする。  
3. シェルで以下のようにjupyerlabを起動する。
```
$ jupyer lab --allow-root
```
4. ブラウザで8888ポートに接続することでjupyter labに接続できる。  

### ディレクトリ構成
#### .decontainerディレクトリ

`devcontainer.json`はリモート開発用のVSCodeの設定を記述する。
そのほかは起動するコンテナ用の`Dockerfile`や`docker-compose`用のファイル。
今回コンテナはひとつなのでdocker-composeは不要ではあるが、他のコンテナを追加したときのために
docker-composeで起動するようにしている。

#### pythonディレクトリ
起動したpythonコンテナがマウントするフォルダで、コンテナの `/tmp/work`以下にマウントされる。

