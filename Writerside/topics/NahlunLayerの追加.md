# NahlunLayerの追加

これまでに、Nahlundのセットアップと、基本的な地図アプリケーションの作成を行いました。
ここでは、作成した地図アプリケーションにNahlunLayerを追加して、Nahlundから配信されたデータを描画できるようにします。

## 依存関係の追加

まず、NahlunLayerを使用するために、依存関係を追加します。

```bash
npm install @azishio/nahlun-layer
```

## NahlunLayerの追加

次に、`App.tsx`を編集して、NahlunLayerを追加します。

`App.tsx`:

```
"use client";

import {DeckGL} from "@deck.gl/react";
import {useRef} from "react";
import {NahlunLayer, NahlunLayerData} from "@azishio/nahlun-layer";

export function App() {

    const nahlunData = useRef(new NahlunLayerData("localhost:3001", "localhost:3002"));

    const layer = new NahlunLayer({
        data: nahlunData.current,
    });

    return (
        <DeckGL
            initialViewState={
                {
                    longitude: 139.0192649,
                    latitude: 36.486692,
                    zoom: 15
                }
            }
            controller
            layers={[layer]}
        >
        </DeckGL>
    );
}
```

`npm run dev`より、地図アプリケーションを起動すると、ブラウザからNahlundから配信されたデータを描画した地図が表示されます。