# Managing Incidents

- この章で説明すること
  - アドホックなインシデント管理のために制御不能になったインシデントの概要
  - 適切に管理されたインシデントに対するアプローチ
  - インシデント管理がうまく機能している場合に同様のインシデントがどのように繰り返されるのか

## The Anatomy of an Unmanaged Incident (管理されていないインシデントの解剖)

- インシデントを制御不能に導く要素がある

### Sharp Focus on the Technical Problem

- 問題解決のためにシステムに変更を加える時の話
- 目の前の技術的な課題に圧倒されて、問題を緩和するための大きな方針を考えないのは良くない

### Poor Communication

- 目の前のことで精一杯でコミュニケーションをしない
- 同僚がお互い何をしているかを知らない

### Freelancing

- 同僚と協力することをしないで勘など頼ってシステムに変更を加える（例え善意であったとしても良くない）

## インシデント管理プロセスの要素

- ちゃんと設計されたインシデント管理のプロセスの特徴
  - 再帰的な責任の分離
    - インシデントに関わる全員が自分の役割を知り、他に人の責任範囲に踏み入らないことが大事
      - こっちの方が自律的に動けるようになる
    - 特定のメンバーの負荷が大きすぎる場合、リーダーに人をよこしてもらって仕事を任せる
    - あるいは、システムのコンポーネントを同僚に任せる
    - **特定の個人に委任されるべき役割の一覧**
      - インシデント対応の指揮官役  
        インシデント対応部隊を編成して、責任を割り当てていく。  
        適切に働けばオペレーション役の障害を排除できる。  
      - オペレーション役  
        実際に作業を行ってインシデントに対応するチーム。  
        インシデントの際にシステムに変更を加えるのはこのチームだけ。  
      - コミュニケーション役  
        対応チームのパイプ役。  
        対応チームとステークホルダーに情報を流し続けたり、報告書を最新の状態に保ったりする。  
      - 計画役  
        バグの報告、夕食の手配、システムが通常状態からどのようにおかしくなったのかを追跡したりなど、長期的な問題に対応する。
  - どこで対応がなされているかが認識されている
    - 多くの場合は、対応メンバーをどこか指定された場所に配置するのが適切
    - IRCは最高（今だとSlackとかかな）
      - ログとして使える、ボットの存在、離れていても大丈夫
  - インシデント状態のドキュメントを最新に保つ
    - 複数人で同時編集できるものが理想（Google Docsとか）
    - 付録Cにドキュメントの例がある
  - 明確かつ即座に役割を交代する

## インシデントの公表時期

- インシデントを早期に宣言してシンプルな修正を行いクローズするのが良い
- インシデントを宣言する条件を明確に定義する
  - 問題を解決するために他のチームに参加する必要があるか？
  - ユーザ影響はあるか？
  - 1時間調査しても問題が解決されていないか？
- インシデント管理能力は絶えず行わないとすぐに萎縮する
  - エンジニアは、どのようにしたらインシデント管理スキルを最新の状態に保ちながらインシデントを処理できるのか？
  - 通常の変更を管理する作業の際に、インシデント管理のフレームワークを用いればインシデントが発生した場合にもフレームワークに従うことができる

## まとめ

インシデント管理戦略を事前に策定し、計画をスムーズに調整し、計画を定期的に使用することで、復旧までの平均時間を短縮し、緊急対応時のストレスを軽減できる。

- 優先順位付け  
  とにかくサービスを復旧させて、根本原因の証拠を保存する
- 準備  
  事前にインシデント管理手順を決めてドキュメント化しておく
- 信頼  
  インシデント対応の関係者に役割の中で自主性を持ってもらう
- 内省  
  インシデント対応中の自分の感情に気を払う。パニックになったりしたら助けを求める。
- 代替案の考慮  
  常に自分が行っていることが意味があるかを考え続ける
- 練習  
  常に決められた手順に従い習慣化する
- 役割を交代する  
  チームメンバー全員がそれぞれの役割ができるようにしておく