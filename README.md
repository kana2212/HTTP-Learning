# HTTP-Learning  
## やること  
HTTPにまつわる用語について調べ、自分なりの言葉で纏める  

### ・URLとは何か、クエリ文字列とは何か 
Uniform Resource Locator（ユニフォームリソースロケータ)の略。ホームページに接続する際の住所のこと  
例えばYahoo!天気情報のアドレスで  
``` https://weather.yahoo.co.jp/weather/?day=2 ```　を例にすると、  
https:// はスキーム名、weather.はホスト名、yahooはドメイン名、coはセカンドレベルドメイン、jpはトップレベルドメイン、  
/weather/はディレクトリ、
/?day=2はファイル名 の要素で成り立つ

?が付いた所からday=2部分はクエリパラメータ（クエリ文字列）  
URLの最後に追加する文字列。検索条件。  
?□=△○　←の様な「名前=値」という書き方になり、値が続く場合は「&」で繋げる。但し「?」を挿入できるのは一度だけ  
検索、フィルタなどに関する条件

### ・パスパラメーターとは何か、クエリパラメータとの違いについて  
ドメインの後の?より前にくる特定のリソースを識別する為に必要な情報。パス(URL)の一部分をパラメータ化して関数部分で利用する事を可能にする仕組み
パスパラメータは**識別**する為、クエリパラメータは特定のリソースを**捜査して取得**する為に必要な情報を表す  

### ・HTTPメソッドとは何か  
クライアントがサーバにしてほしいことを依頼する為の手段  
GET/POST/PUT/PATCH/DELETEなどの働きを持つメソッドの総称  

  --- GETの意味  
指定したリソースの取得をする、レスポンスステータスは成功すると200を返す  
使用例・・・API経由でデータを取得、画像データの取得  

  ---POSTの意味  
  リソースへのデータ送信、サーバー上の状態の変更、レスポンスステータスは成功すると201を返す  
  使用例・・・web上のフォームからデータを送る、SNSなどアカウントを新しく作る 
  
  ---PATCHの意味  
  データが既に存在しているものに対して更新をかける処理の事。部分的な更新。冪等性はない  
  
  ---DELETEの意味  
  既存データの削除を行うときに使用する、レスポンスステータスは204 No Contentを返す  
  使用例・・・ブログ記事の削除、既存アカウントの削除  
  
  ### ・HTTPステータスコードとは何か 
  URLで送ったリクエストに対し、サーバーからのレスポンスを表す数字の事  
  
  ---200の意味  
  GETリクエストをした際にリソースが正常に読み込まれ成功した事を表す  
  
  ---201の意味  
  POST,PUTリクエストでリクエストが成功し、結果新たなリソースが作成された事を表す  
  
  ---400の意味  
  Bad Request　構文無効でサーバーがリクエストを理解できない時に表示される。リクエスト内容の見直しが必要  
  
  ---404の意味  
  Not Found ブラウザーではURLが解釈出来なかった事を意味する。ページが見つからない状態  
  
  ---500の意味  
  サーバー側で処理方法が分からない事態が発生。サーバー内のプログラムに記述されている内容に誤り、エラーがある  
  
  ### ・リクエストヘッダーとは何か  
  HTTPリクエストで使用されるHTTPヘッダーの事。HTTPリクエストを構成する3つの部品の一つ  
  HTTPリクエスト前半にある制御情報を記した領域で、要求内容の詳細が書かれている  
  主なフィールドはホスト、参照元URL、Cookie、Authrizationなどがある
  
  ### ・リクエストボディとは何か  
  HTTPリクエストを構成する部品で、主に捕捉情報が書かれている。POSTリクエストの場合は受け渡すパラメータの内容が書かれる  
  
  ### ・レスポンスヘッダーとは何か  
  HTTPレスポンスを構成する部品の一つ。HTTPステータスラインに書ききれないレスポンス情報が書かれている  
 [フィールド名] : [内容] といった書式で記述される。Content-Typeやリクエストをした日時などを示す  
  
  ### ・レスポンスボディとは何か、JSONとは何か   
  APIがクライアントに送るデータ。{}の中身。下図で言うと選択された青い範囲を指す。JSON形式  
  
  JSONはJavaScript Object Notationの略。データを記述する為のフォーマット。ファイルはテキスト形式ファイルで拡張子は.json  
  表記形式は {"名前" : "値"}  
  名前と値の間は:(コロン)を入れる。データが複数ある場合は,(カンマ)で繋ぐ  
  
  ![JSON リクエストボディ](https://user-images.githubusercontent.com/121325913/224718058-f14458ac-a329-4084-a2ad-476fb3a97021.png)

  
  



