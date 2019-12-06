# Docker Hands-on Workshops
## Use Images

xxx

<a><img src="images/docker-containerized-and-vm-transparent-bg.png" width="878" height="400"></a>

# 環境を使う
## study1:用語解説

## step1:環境の中を動き回る
### Docker Compose
#### コンテナの起動

```
$ docker-compose start
```

#### コンテナの停止

```
$ docker-compose stop
```

#### コンテナの一覧表示

```
$ docker-compose ps
```
- Name列にサービス名が表示されます。

#### コンテナのログ確認

```
$ docker-compose logs <サービス名>
```
- 「docker-compose ps」コマンドでサービス名を確認します。

### コンテナの中に入ってみる

```
$ docker-compose exec container1 /bin/bash
```

- コンテナの中でシェルを起動し、ターミナルとつなぎます

```
$ echo 'ok' > testfile
$ cat testfile
$ ls testfile
```

- そのほかいろいろやってみてください

```
$ exit
```

 - でbashを終了してコンテナから抜けられます

### コンテナを止めてみる

```
$ docker-compose down
```

- docker-compose.ymlに記述されたコンテナを停止します

```
$ docker ps
```

- kitematicを実行して現在の状態を確認してみてください。

```
$ docker-compose exec container1 /bin/bash
```

- エラーが出ます。コンテナが起動していないので動かせません

### コンテナを停止するとまっさらの状態に戻る

```
$ docker-compose up -d
```

```
$ docker-compose exec container1 /bin/bash
```

```
$ cat testfile
```

```
$ ls testfile
```

- 先程書き込んだファイルですが存在しません
- 同じImageを使った別のコンテナなので、まっさらの状態に戻っています

```
$ exit
```

- で終了します

### コンテナを足してみる

## study2:登場人物を把握する
### Image
### Container
### Process

- ルートプロセスはコンテナの作成時にEntrypointとして起動されたプロセス

- 通常の独立したLinuxシステムでは、伝統的に/bin/initが起動時に実行されますが、Dockerコンテナではもっとシンプルな初期起動スクリプトを都度書くことが慣習です

```
$ docker-compose logs -f
```

- ルートプロセスの標準出力・標準エラー出力が集約されて表示されます

### Volume
### Port

[事前準備](/docker/001-Preparation/) ← 戻る [トップへ](..)　　つづき → [環境を作る](/docker/003-CreateImage/) 