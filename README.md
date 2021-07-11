# VS Codeを使ったコンテナでのリモート開発環境

## VS Codeを使った起動方法

1. C-S-pでコマンド入力を開き、Remote-Containers:Reopen in Containerコマンドを起動する。  
2. コンテナが起動しコンテナ内に起動したシェルがオープンする。  
3. シェルで以下のようにjupyerlabを起動する。
```
$ jupyer lab --allow-root
```
4. ブラウザで8888ポートに接続することでjupyter labに接続できる。  

### ディレクトリ構成
