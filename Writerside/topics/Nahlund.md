# Nahlund

Nahlundは、Nahlunのうちサーバーで動作するサービスです。
水位計からのデータを受信し、3Dデータを生成してクライアントに配信します。

![Nahlunの概要](ov-nahlund.drawio.svg)

## 依存関係

Nahlundのインストール/実行には以下の依存関係が必要です。

+ [curl](https://curl.se/)
+ [docker](https://docs.docker.com/get-started/get-docker/)
+ [docker-compose](https://docs.docker.com/compose/install/)

## インストール

### 河川データの取得

Nahlundは、河川の3Dデータを生成するために、河川のデータを使用します。
以下のコマンドで、Nahlundに必要なデータを取得できます。

```console
curl -L https://raw.githubusercontent.com/azishio/rnet/refs/heads/main/run.sh | bash
```

> このスクリプトの実行には、数十分から数時間かかる場合があります。
> また、多くのデータをダウンロードするため安定したネットワーク環境が必要です。
>
{style="note"}

### サービスのインストール

Nahlundの実態は、docker-composeにより構築されたコンテナ群をsystemdでサービス化したものです。

以下のインストールスクリプトを実行することで、Nahlundをシステムにインストールできます。
スクリプトの内容を理解した上で実行してください。

```console
curl -L https://raw.githubusercontent.com/azishio/nahlund/refs/heads/main/install.sh | bash
```

以下のコマンドでシステムにNahlundサービスがインストールされていることを確認できます。

```console
systemctl status nahlund
```

### サービスの起動

以下のコマンドでNahlundサービスを起動できます。

```console
systemctl start nahlund
```

以下のコマンドでNahlundサービスが正常に起動していることを確認できます。

```console
systemctl status nahlund
```
