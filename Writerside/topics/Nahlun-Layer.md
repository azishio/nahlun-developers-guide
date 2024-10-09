# Nahlun Layer

![Nahlunの概要](ov-nahlun-layer.drawio.svg)

Nahlun Layerは、Nahlundからデータを受け取り、3D地図上に河川の水位を表示するためのDECK.GLのレイヤーです。
これを使用することで、任意の地図アプリケーションに河川水位の可視化機能を追加することができます。

## インストール

<tabs>
    <tab title="npm">
        <code-block lang="console">
            npm install @azishio/nahlun-layer
        </code-block>
    </tab>
    <tab title="pnpm">
        <code-block lang="console">
            pnpm install @azishio/nahlun-layer
        </code-block>
    </tab>
    <tab title="yarn">
        <code-block lang="console">
            yarn add @azishio/nahlun-layer
        </code-block>
    </tab>
    <tab title="bun">
        <code-block lang="console">
            bun add @azishio/nahlun-layer
        </code-block>
    </tab>
</tabs>

## Peer Dependencies

[deck.gl](https://www.npmjs.com/package/deck.gl)と[socket.io-client](https://www.npmjs.com/package/socket.io-client)
は、Nahlun Layerの依存関係として必要です。
現在は以下のバージョンでのみ動作確認を行っていますが、より古いものでも動作する可能性があります。
今後古い依存環境下での動作確認を進め、peerDependenciesの範囲を広げる予定です。

```json
{
  "peerDependencies": {
    "deck.gl": "^9.0.33",
    "socket.io-client": "^4.8.0"
  }
}
```

## Example

<tabs>
    <tab title="React">
        comming soon...
    </tab>
    <tab title="JavaScript">
        comming soon...
    </tab>
    <tab title="TypeScript">
        comming soon...
    </tab>
</tabs>