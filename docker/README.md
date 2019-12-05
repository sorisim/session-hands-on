# Docker Hands-on Workshops

<a><img src="images/handson.jpg" width="768" height="576"></a>

- 前提とする知識レベル
  - 通常のLinuxシステムについての基本的な理解
  - SSHによってHTTPサーバの簡易なメンテナンスができる

# Dockerハンズオン目次

| Title | Description | Learning Time | Teaching Time With Discussion | 
| :------- | :---------- | :-- | :-- |
| [事前準備](001-Preparation/)  | このワークショップでは、ハンズオン参加者はDockerコンテナを稼働させるためのホストサーバおよびネットワークからなるハンズオン環境をAWS上に準備します。CloudFormationを利用して宣言的にハンズオン環境を構築することができます。ホストにはSSH接続を行います。ハンズオン参加者は鍵ペアを事前に準備する必要があります。 | 10 min | 20 min |
| [環境を使う](002-UseImage/)  | 様々なOSSミドルウェアについて、Dockerイメージを取得し手軽にサービスを立ち上げる体験をします | 10 min | 20 min |
| [環境を作る](003-CreateImage/)  | dockerfileを利用してDockerイメージを生成し、任意の内容のDockerコンテナを立ち上げる体験をします | 10 min | 20 min |
| [揮発性を理解する](004-KnowVolatility/)  | Dockerコンテナの内部で更新が発生した場合の結果の保持について理解します | 10 min | 20 min |