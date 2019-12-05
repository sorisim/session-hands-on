# Docker Hands-on Workshops
## Use Images

xxx

<a><img src="images/docker-containerized-and-vm-transparent-bg.png" width="878" height="567"></a>

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
### コンテナを止めてみる
### コンテナを停止するとまっさらの状態に戻る
### コンテナを足してみる

## study2:登場人物を把握する
### Image
### Container
### Process
### Volume
### Port

[事前準備](/docker/001-Preparation/) ← 戻る [トップへ](..)　　つづき → [環境を作る](/docker/003-CreateImage/) 