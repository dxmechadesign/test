```mermaid
graph TD
    A[開始] -->|configdataが配列か?| B{配列の確認}
    B -- はい --> C[バッファをconfigInstanceのサイズで割り当てる]
    B -- いいえ --> Z[終了]
    C --> D{configdataを反復処理する}
    D --> E{dataArrayが配列か?}
    E -- はい --> F[バッファにdataArrayの値を埋める]
    E -- いいえ --> G{値のタイプを決定する}
    G --> H{タイプとサイズに基づいて値を計算する}
    H --> I[バッファに計算された値を書き込む]
    I --> J{さらにデータはあるか?}
    J -- はい --> D
    J -- いいえ --> K[バッファをconfigInstance.dataに割り当てる]
    K --> L[スキャナーノードを取得する]
    L --> M[設定で接続を追加する]
    M --> N['close'イベントを処理する]
    N --> Z
```
