# Docker Hands-on Workshops
## Preparation

<a><img src="images/preparation.jpg" width="878" height="567"></a>

AWS
================================
ここではハンズオン参加者それぞれのAWSアカウントにDockerハンズオン環境を構築します。
Docker用インフラ環境はCloudFormationにより自動的に生成されます。

- [アーキテクチャ](#アーキテクチャ)
- [事前準備](#事前準備)
- [オペレーション](#オペレーション)


## アーキテクチャ

## 事前準備

### 作業PC

- sshコマンドが使えるターミナルを準備します。
- ssh鍵ペアを準備します。

## オペレーション

### AWS

- AWSマネジメントコンソールにログインします。
- EC2画面を開きます。キーペアにて公開鍵を登録します。
- CloudFormation画面を開きます。

### CloudFormation

- [CloudFormationテンプレート](AWS.CloudFormation/Docker.yml) を登録します。

## スタックの実行
## インスタンスへのログイン

[トップへ](..)　　つづき → [環境を使う](/docker/002-UseImage/) 