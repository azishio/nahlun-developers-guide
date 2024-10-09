# Nahlun Developer's Guid

## このガイドについて

このガイドでは、[DECK.GL](https://deck.gl)を使用した独自の地図サービスに河川水位の三次元可視化機能を組み込む方法を紹介します。

> 本マニュアルは、以下の知識を持つ人を対象としています
> + Linuxに関する基礎知識(特に、シェルの操作)
> + TypeScriptを使用したWebアプリケーションの実装方法
> <br/>
> また、以下の経験があると、より理解が簡単になります
> + [MapLibre](https://maplibre.org)や[DECK.GL](https://deck.gl)を使用したWebアプリケーションの実装
>
{style="note"}

## Nahlunとは
Nahlunは、日本の河川水位を3Dで可視化するためのプロジェクトです。
このプロジェクトは水位計を管理して3Dデータを配信するサーバーアプリケーションと、3Dデータを表示するクライアントコンポーネントから構成されています。

![Nahlunの概要](overview.drawio.svg)


## リポジトリ
| Name         | URL                                         |
|--------------|---------------------------------------------|
| Nahlund      | [](https://github.com/azishio/nahlund)      |
| Nahlun Layer | [](https://github.com/azishio/nahlun-layer) |