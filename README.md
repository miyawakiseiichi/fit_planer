# # 0601_SM
■サービス概要
どんなサービスなのかを３行で説明してください。
  筋トレをするうえで、初心者の方がまず初めに困ってしまうのが『なにからやればいいか？』『どの様にすればいいのか？』が考えられます。
  また、中級者では『フォームが正しいのか？』『本当に成長しているのか？』『壁にぶつかった時の打開策は？』というものが考えられます。
  これらの疑問や筋トレのメニュー・カロリー制限制限(ダイエット用)を解決、またサプリメントやプロテインなどもサポートするためのサービスです。

■ このサービスへの思い・作りたい理由
このサービスの題材となるものに関してのエピソードがあれば詳しく教えてください。
  自分の趣味が筋トレでその時にこんなサイトがあればいいなと思い作成してみようと思いました。
このサービスを思いつくにあたって元となる思いがあれば詳しく教えてください。

■ ユーザー層について
決めたユーザー層についてどうしてその層を対象にしたのかそれぞれ理由を教えてください。
  10代〜50代
  ・10代 部活動や成長の邪魔にならない程度のトレーニングを必要としているユーザー
  ・20代 30代 40代 50代 男女問わずダイエット・健康維持を必要としているユーザー

■サービスの利用イメージ
ユーザーがこのサービスをどのように利用できて、それによってどんな価値を得られるかを簡単に説明してください。
  筋トレをするうえでのカレンダーでの筋トレメニューの管理・進行状況でのモチベーション維持・疑問の解決というサービスが利用できて、それにより継続的に筋トレを続けることができる。

■ ユーザーの獲得について
想定したユーザー層に対してそれぞれどのようにサービスを届けるのか現状考えていることがあれば教えてください。
  各ユーザーに初め新規登録としてユーザー情報の他にプランを選択していただきます。単純にダイエットなのかそれとも、ムキムキになりたいのかでメニューやサプリメント、プロテインが変わってくるからです。

■ サービスの差別化ポイント・推しポイント
似たようなサービスが存在する場合、そのサービスとの明確な差別化ポイントとその差別化ポイントのどこが優れているのか教えてください。
独自性の強いサービスの場合、このサービスの推しとなるポイントを教えてください。
  サプリやプロテインの飲み合わせや味、飲むタイミングも通知したり、カレンダーと同期させメニューやセット数も決めてくれる。休息の時間も開始〜終了と通知が入りトレーニング中に時間を無駄にすることはない。
  自動で決められるメニューにプラスしてタスクを追加できる。また筋肉をつける以外に健康維持でも使用できるように高齢の方までユーザーを確保できる。
■ 機能候補
現状作ろうと思っている機能、案段階の機能をしっかりと固まっていなくても構わないのでMVPリリース時に作っていたいもの、本リリースまでに作っていたいものをそれぞれ分けて教えてください。

   MVP
    会員登録
    ログイン
    プラン一覧
    プラン登録
    プラン詳細 ※プランとはこのアプリをなに目的で使用するか
              ・ダイエット
              ・健康維持
              ・ゴリマッチョ
    
   その後
    プラン公開  筋トレメニュー
    タグ機能  カレンダー・筋トレ種目一覧・各部位の筋肉の説明
    タスク機能  自動で決められたメニュー以外の自分で決めるメニューの追加・削除
    検索機能  使用するプロテインやサプリ


■ 機能の実装方針予定
一般的なCRUD以外の実装予定の機能についてそれぞれどのようなイメージ(使用するAPIや)で実装する予定なのか現状考えているもので良いので教えて下さい。
・通知
  WebSocket通信・ActionCable（Rails標準）LINE Messaging API SDK for Ruby
    https://github.com/line/line-bot-sdk-ruby

・検索
  Stimulus Autocomplete（Rails7 ）
    https://github.com/afcapel/stimulus-autocomplete

・画像加工・合成
  RMagick
    https://github.com/rmagick/rmagick

・位置情報
  Google Maps Platform
    https://mapsplatform.google.com/intl/ja/

・タスク
  Firebase

・カレンダー
  Google Calendar API

### 画面遷移図
Figma：https://www.figma.com/design/v74Oa4k0MQGRp1HbND0XRv/Untitled?node-id=0-1&t=eIuS5VEl64blnYRf-1

### READMEに記載した機能
- [x] トップページ
- [x] プラン決定
- [x] 質問
- [x] 週間メニュー
- [x] 会員登録
- [x] ジム検索一覧
- [x] ジム詳細
- [x] タスク作成・削除
- [x] ログイン
- [x] マイページ
- [x] ユーザー登録ページ
- [x] 登録完了
- [x] サプリメント検索一覧
- [x] サプリメント詳細
- [x] プロテイン検索一覧
- [x] プロテイン詳細
- [x] お問い合わせ入力
- [x] お問い合わせ内容の確認
- [x] お問い合わせ完了

### 本サービスの概要
筋トレ初心者から中級者までを対象としたトレーニングサポートアプリです。初心者が抱える「正しいフォームがわからない」といった悩みや、中級者の「成長が停滞している」
「壁が越えられない」といった課題を解決します。このアプリでは、目的に応じたプラン（例：ダイエット・健康維持・筋力アップ）を選択し、自動生成されたトレーニングメ
ニューや栄養管理をカレンダー形式で一括管理できます。また、サプリメントやプロテインの検索、摂取タイミング通知機能も備え、効率的なトレーニングをサポートします。
初心者向けのシンプルなガイドだけでなく、カスタマイズ可能なメニュー作成や進歩データの可視化機能により、中級者の継続機な成長を支援します。さらに、Google Mapsに
よるジム検索や問い合わせ機能を提供し、幅広いユーザーに利用可能な設計が特徴です。

### MVPで実装する予定の機能
- [x] 会員登録機能 2
- [x] ログイン機能 2
- [x] プラン一覧機能 2
- [x] プラン登録機能 3
- [x] プラン詳細機能 2
- [x] マイページ機能 3
- [x] トップページ機能 2
- [x] 登録完了画面機能 1
- [x] お問い合わせ入力機能 3
- [x] お問い合わせ確認機能 2
- [x] お問い合わせ完了画面機能 1

### 1週間辺りの開発に向けられる時間
- 1週間あたり: 約30時間

### ProjectsのURL
https://github.com/users/miyawakiseiichi/projects/1

### MVP後
- [x] タグ機能（カレンダー・筋トレ種目一覧・部位別説明） 5
- [x] カレンダー機能との連携 8
- [x] サプリメントやプロテインの検索・通知機能 5
- [x] タスク機能（トレーニングメニューの追加・削除 3
- [x] GoogleMap 5

### MVPレビュー依頼予定日
予定日: 2024年 1月 7日