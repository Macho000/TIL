# Translating Embedding for Modeling Multi-relational Data
- 通称TransEと呼ばれるもの
- 目標：カノニカルモデル（訓練しやすく、パラメータの数を減らし、大きなデータベースに拡大しやすいモデル）を提案すること
- カノニカルモデルとはデータ共有モデル
  - A canonical model is a design pattern used to communicate between different data formats quoted by Wikipedia
  - 異なるデータ間の通信に用いられるデザインパターン

## Introduction
- Multi-relational data：(head,label,tail)で表される。
  -　Multi-relation dataは様々な分野で重要な役割を果たしている
    - SNS分析　ー>　人と人の関係が友達なのか、社会的なつながりなのか？
    - 推薦システム　ー>　商品と購入者の関係が買ったのか、評価したのか、レビューしたのか、探したのかなど
    -　Knowledge bases(KBs)　Ex. Freebase, Google Knowledge Graph or GeneOntology　
      - 知識ベースでは、KBの各エンティティが世界の抽象的な概念または具体的なエンティティを表し、関係は2つのエンティティが関わる事実を表す述語です
    - この論文ではMulti-relational dataをKBｓから構築し、自動的にノードを作成、エッジを生成するツールを作ることを目標にしている

- モデリングのプロセスは、エンティティ間のローカルまたはグローバルな接続性パターンを抽出することに集約され、予測は、これらのパターンを使用して、特定のエンティティと他のすべてのエンティティとの間で観察された関係を一般化することによって行われます
  - つまり、Multi-relational dataを作るに当たり、Entity(ノード)間の関係性を既存の接続パターンから予測すること？
  
 -  Relationships as translations in the embedding space
  - TransE：
    - エンティティの低次元の埋め込み表現を学習するためのエネルギーベースモデル
    - リレーションシップは埋め込み空間で変kなんされた形で表現される
    - （h，l，t）が成り立つなら、tailエンティティtはheadエンティティとリレーションシップlとの和の埋め込み表現と近くなるべき
    - この論文では、パラメータの数をへらすことに注力した、具体的には、一つの低次元のベクトル表現をエンティティとリレーションシップをすべて学習する事によって実現
    - 
    
    
