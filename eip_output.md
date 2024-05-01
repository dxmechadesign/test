'''marmaid
graph TD
    A[開始] --> B[Nodeの作成]
    B --> C[接続の取得]
    C --> D[変換関数convert2の定義]
    D --> E[入力イベントの処理]
    E --> F{データタイプによる分岐}
    F -->|UInt8| G[UInt8として書き込む]
    F -->|Int8| H[Int8として書き込む]
    F -->|UInt16| I[UInt16として書き込む]
    F -->|Int16| J[Int16として書き込む]
    F -->|UInt32| K[UInt32として書き込む]
    F -->|Int32| L[Int32として書き込む]
    F -->|Float| M[Floatとして書き込む]
    F -->|Bit| N[ビット操作を行い書き込む]
    G --> O[メッセージ送信]
    H --> O
    I --> O
    J --> O
    K --> O
    L --> O
    M --> O
    N --> O
    O --> P[終了処理の実行]
    P --> Q[接続ステータスの更新]
    Q --> R[終了]
'''
