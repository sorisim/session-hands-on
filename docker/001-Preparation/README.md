# Docker Hands-on Workshops
## Preparation

<a><img src="images/preparation.jpg" width="878" height="567"></a>

AWS
================================
ここではハンズオン参加者それぞれのAWSアカウントにDockerハンズオン環境を構築します。
この環境はCloudFormationにより自動的に生成されます。

- [アーキテクチャ](#アーキテクチャ)
- [事前準備](#事前準備)
- [ハンズオン当日](#ハンズオン当日)


## アーキテクチャ

## 事前準備

### 作業PC

- sshコマンドが使えるターミナルを準備します。
- ssh鍵ペアを準備します。

### AWS

- ハンズオン参加者それぞれがAWSアカウントを取得する必要があります。アカウントは無料で作成することができます（クレジットカードが必要）
- アカウント作成時から1年間、特定の機能を無料で利用することができます

https://aws.amazon.com/jp/s/dm/landing-page/create-free-account/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc


## ハンズオン当日
### 作業PC

- このリポジトリの [CloudFormationテンプレート](AWS.CloudFormation/Docker.yml)を 作業PC内に保存します。12行目のIPアドレスをパブリックIPアドレスで書き換えます。



### AWS

- AWSマネジメントコンソールにログインします。
- EC2画面を開きます。キーペアにて公開鍵を登録します。
- CloudFormation画面を開きます。

## CloudFormation

- AWSマネジメントコンソールにアクセスします。
  - S3にアクセスし、テンプレートファイルをアップロードします。バケットが無ければ、新しくバケットを作成します。
  - 更新した[CloudFormationテンプレート](AWS.CloudFormation/Docker.yml) をアップロードします。
  - アップロードの後、テンプレートファイルを選択し、リンクをコピーします。

### スタックを実行してAWSリソースを作成します

- CloudFormationにアクセスし、スタックを作成します。
  - 「新しいスタックの作成」を選択します。
  - アップロードしたテンプレートファイルを選択します。
  - パラメータを設定します。リソース関連は事前準備で作成したものを指定します。
    - スタックの名前
      - 任意の名前を入力します。
    - InstanceType
      - 「t2.micro」は個人の1年間無料枠内で利用できます。ただしメモリが1ギガしか使用できません。
    - MyIP
      - Dockerハンズオン環境へのアクセス元となるソースIPのCIDRを指定します。
    - KeyName
      - キーペアにて登録した公開鍵の登録名を選択します。
  - 以降は「次へ」を選択し、作成します。大体3分ぐらいで完了します。
    - 状況がPROGRESSからCOMPLETEになれば作成完了です。右上の更新ボタンで表示を更新できます。
      - EC2にアクセスし、各EC2インスタンスを選択して、パブリックIPを確認します。

## インスタンスへのログイン

  - 確認したパブリックIPアドレスを接続先として、CloudFormationに登録したキーペアでSSHログインを行います。
  - これで事前準備は終わりです。お疲れさまでした。
  - ハンズオンでの操作はSSHでサーバアクセスして、docker / docker-composeコマンドで行います。
    - docker-composeのコマンドは[コマンドリファレンス](http://docs.docker.jp/compose/reference/toc.html)を見てください。

[トップへ](..)　　つづき → [環境を使う](/docker/002-UseImage/) 