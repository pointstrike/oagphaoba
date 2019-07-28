python、opencvで画像のフーリエ変換と逆変換を行い、元の画像に復元するプログラムです。価値や意味はないです。

当方の勉強不足により、マウスによるマスク画像作成、および対応するフーリエ変換波形のリアルタイム加算機能はありません。







### 実装した処理
- フーリエ変換
画像をフーリエ変換し、複素数領域を含めて数値の塊を画像化します。

- フーリエ逆変換
フーリエ変換で作り出した数値の配列から、元の画像を復元します。

    
### 使い方，実行の仕方，依存ライブラリとバージョン 
実行の仕方：

　pythonの環境構築、cmdから必要なopencv関連のインポートを行う。その後、各環境から起動します。
 
 


### 使い方：

　画像名の部分のパスを変更して起動すると、出力側に元画像とフーリエ変換後の画像が表示され、ウィンドウ側にはフーリエ逆変換終了後の画像が表示されます。ウィンドウは0または×ボタンで終了できます。

### 参考にしたサイトなどへのリンク
 ｰ http://www.hello-python.com/2018/02/16/numpyとopencvを使った画像のフーリエ変換と逆変換/

### 参考部分
1. フーリエ変換、逆変換の実装
ｰ http://www.hello-python.com/2018/02/16/numpyとopencvを使った画像のフーリエ変換と逆変換/
- 以上リンクのほぼすべてを引用させていただきました。

### 作りたかった機能
 - マウスで一点を指定して、フーリエ変換後の画像の波形を調べる機能
    - ｢画像の座標を取得するプログラム｣と、今回のプログラムにおける、配列"fimage"から取得した、画像の点に対する複素数を、｢複素数をsin波形として"画像化"する｣プログラムに通すことで、実現することができるのではないかと推察した。
    - 実際は、複素数から作り出したsin波を画像化する方法が分からなかった。
    
    
 - マウスで塗りつぶした部分の黒塗りを解除して、逆のマスクとすること。
    - ｢白黒(または0-1のみ)のお絵かき系のプログラム｣に変更を加えれば実装できるのではないかと推察した。
    - 実際は、そんなプログラムは見つけることが出来なかった。
 
 - 上で作り出したマスクをフーリエ変換にかぶせ、復元した各sin波を加算し続ける機能。
    - 上のプログラムの変更部分をリアルタイムで読み込み、対応するフーリエ逆変換を常に加算し続ける→逆変換画像を表示するのループを常に行うことで、実装できる のではないかと推察した。
    - 実際は、上のプログラムが完成しなかったので、取り組むこともできなかった。
