### 概要
- Python実行用Dockerコンテナ
- python version 3.11.7
- Amazon Linux release 2023

### インストール用URL
* Amazonlinux
https://hub.docker.com/_/amazonlinux/

* pyenv
https://github.com/pyenv/pyenv/wiki

### 利用手順
```
# ディレクトリ移動
cd docker-python

# 起動
docker-compose up -d

# docker接続
docker exec -it python.local bash --login

# 停止、削除
docker-compose down --rmi all --volumes --remove-orphans
```