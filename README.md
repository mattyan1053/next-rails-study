# What is this ?

mattyan1053によるWeb開発練習用リポジトリ
- Frontend: Next.js
- Backend: Ruby on Rails
- Database: MySQL

# Environment
動作確認済みOS
- Rocky Linux release 8.6 (Green Obsidian)

# Usage
Docker, docker composeがインストールされていれば、自動で環境構築します。

```sh
# イメージのビルド
$ docker compose build
# コンテナの起動
$ docker compose up -d
```

# Appendix
Rocky Linux でのdocker周りインストール方法と確認バージョン
## Docker Installation
```sh
# リポジトリの追加
$ sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
# リポジトリ確認
$ sudo dnf repolist
# Docker のインストール
$ sudo dnf install -y docker-ce
# Dockerを使えるユーザの追加
$ sudo usermod -aG docker [username]
# インストール確認
$ docker version
Client: Docker Engine - Community
 Version:           20.10.17
 API version:       1.41
 Go version:        go1.17.11
 Git commit:        100c701
 Built:             Mon Jun  6 23:03:11 2022
 OS/Arch:           linux/amd64
 Context:           default
 Experimental:      true

Server: Docker Engine - Community
 Engine:
  Version:          20.10.17
  API version:      1.41 (minimum version 1.12)
  Go version:       go1.17.11
  Git commit:       a89b842
  Built:            Mon Jun  6 23:01:29 2022
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.6
  GitCommit:        10c12954828e7c7c9b6e0ea9b0c02b01407d3ae1
 runc:
  Version:          1.1.2
  GitCommit:        v1.1.2-0-ga916309
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

## Docker Compose Installation
```sh
# Docker compose のインストール
$ sudo dnf install -y docker-compose-plugin
# インストール確認
$ docker compose version
Docker Compose version v2.6.0
```
