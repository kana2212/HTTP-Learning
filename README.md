# HTTP-Learning  
## やること  
HTTPにまつわる用語について調べ、自分なりの言葉で纏める  

### ・URLとは何か、クエリ文字列とは何か 
Uniform Resource Locator（ユニフォームリソースロケータ)の略。ホームページに接続する際の住所のこと  
例えばYahoo!天気情報のアドレスで　``` https://weather.yahoo.co.jp/weather/?day=2 ```　を例にすると、  
https:// はスキーム名、weather.はホスト名、yahooはドメイン名、coはセカンドレベルドメイン、jpはトップレベルドメイン、/weather/はディレクトリ、
/?day=2はファイル名 の要素で成り立つ

?が付いた所からday=2部分はクエリパラメータ（クエリ文字列）  
URLの最後に追加する文字列。検索条件。　?□=△○　←の様な「名前=値」という書き方になり、値が続く場合は「&」で繋げる。但し「?」を挿入できるのは一度だけ  

### ・パスパラメーターとは何か  

