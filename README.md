# これはなに？  
[IkaLog](https://github.com/hasegaw/IkaLog)と連携してニコ生にコメントを投稿する
[NiconamaCommentViewer](http://www.posite-c.com/application/ncv/) (通称NCV) 向けのプラグインです。   
IkaLogのWebSocketServerを利用してデータを取得しています。  
  
# なにができる？  
NCVを通して、IkaLogのイベントの発生に合わせてニコ生に投稿者コメントを投稿する事ができます。  
(イベントの例：イカを倒した、何かに倒された、ゲームの結果、など)  
# 使い方は？  
こちら(Comming soon...)からファイルをダウンロードし、NCVのpluginsフォルダに中身を全て配置してください。  
NCVを起動して、プラグインメニューにIkanama4NCVが出現すれば導入は成功です。  
#### 1. メニューをクリックしてウインドウを開きます。  
#### 2. IkaLogを立ち上げ、WebSocketServerを有効にします。(IkaLog側の設定ウインドウから探してください。CUI版使ってる人は言われなくても頑張ってください。)
#### 3. 真ん中上のそれっぽいボタンを押して、"IkaLogへ接続しました"と表示されればOKです。(2の手順をやったのに出来ない場合はたぶんファイアウォールです)  
#### 4. NCVが放送に接続していない状態でも単体で動作確認をすることが出来ます。設定を行ったあとの動作確認を行いたいときにご活用ください。
### 5. NCVで放送に接続し、スプラトゥーンをプレイしてください。

- 設定について  
NCVの設定メニューに"Ikanama4NCV"の設定が追加されています。  
これをクリックすると、各イベント発生時にコメントを投稿するかどうかと、投稿するコメントの内容を設定することが出来ます。  
このコメント設定部分には変数を使うことが出来ます。これを使うと投稿内容をそれなりに自由にカスタマイズできます。   
- 例:  
 {rule}の{stage}で{weapon}を使って{kills}キル{deaths}デスで{won}ました！  
 -> ナワバリバトルのホッケふ頭でホットブラスターを使って4キル2デスで勝ちました！  
 {reason}でやられた！現在{deaths}デス  
 -> .96ガロンデコでやられた！現在2デス  

 種類は以下のとおりです。(特定のイベントでしか使えないものもあります。どれがどうだったかは今後追加します。。。)  
  
*{weapon}* 自分が使用している武器名   
*{reason}* 何によってやられたか  
*{kills}* 現在のキル数  
*{deaths}* 現在のデス数  
*{rule}* 現在遊んでいるルール名(ナワバリバトル、ガチエリア、等)  
*{stage}* ステージ名  
*{won}* 「勝ち」、もしくは「負け」のどちらか  
  
# 動作環境は？  
NCVはバージョン0.155.3.139で動作確認しています。  
他の環境は試してないのでよくわからないです・・・(動かなかったら言ってちょ)  
ちなみに、制作環境は以下のとおりです。  
- **OS** Windows10 64bit Build 14393.10
- **IDE** Visual Studio 2015 Community  
- **CPU RAM** いまどきこの情報いる？

# 注意  
ここまで読んでくれてありがとうございます。そんな優しい人に対して言うにはちょっと気が引けるけど一応・・・

処理の都合上何秒かラグが出るので難しいとは思うけど、ズルには使わないでね。  
あと、これを使うことによって生じた損害に関して作者([@happou31](https://twitter.com/happou31))は一切の責任を負わないよ。お決まりだね。  

IkaLog本体の棒読みちゃん機能と読み上げが被ってウザい等の場合は、NCV側で投稿者コメントを読みあげない設定をしてください。  
騒がしくていいかもしれないけど。  

-----
TODO 足りない部分そのうち書き足す予定・・・