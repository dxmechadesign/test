```mermaid
graph TD
    A[Node-RED] -->|取得| B[InNode]
    B -->|バイナリデータ変換| C{convert2関数}
    C -->|UInt8| D[UInt8読み取り]
    C -->|Int8| E[Int8読み取り]
    C -->|UInt16| F[UInt16読み取り]
    C -->|Int16| G[Int16読み取り]
    C -->|UInt32| H[UInt32読み取り]
    C -->|Int32| I[Int32読み取り]
    C -->|Float| J[Float読み取り]
    C -->|Bit| K[Bit読み取り]
    D --> L[データ送信]
    E --> L
    F --> L
    G --> L
    H --> L
    I --> L
    J --> L
    K --> L
    L --> M[Node-REDフロー]
    B --> N[接続ステータス更新]
    N --> O[接続]
    N --> P[切断]
```
