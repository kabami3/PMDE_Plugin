▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●

　PMD/PMXウェイト自動設定用プラグイン　ver1.00

▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●▼●


▼▼▼▼　概要　▼▼▼▼

ボーンから頂点へのウェイト設定を自動でやってくれるプラグインです。


▼▼▼▼　使い方　▼▼▼▼

PMDエディタの実行ファイルがある場所に_pluginというフォルダがあります。そこに
"PMDEditor/_plugin/User/AutoWeightComplement.dll"
"PMDEditor/_plugin/User/AutoWeightExclusive.dll"
というように、.dllファイルを全て放り込みます。
PMDエディタを起動後、
"編集/プラグイン/User/ウェイト自動設定(補完的)"
"編集/プラグイン/User/ウェイト自動設定(排他的)"
という項目が出来ているはずなので、押すと自動でウェイト設定がされます。

▼▼▼▼　仕様・注意　▼▼▼▼
※注意
　このプラグインにはUndoが出来ません。全ての頂点ウェイトを書きかえるため、バックアップを取るなどして適当に対応して下さい。
　あくまでボーン作成後にとりあえず仮設定をする時用と割りきって下さい。使った後は自分で細かく設定をすることを推奨します。

補完的：
　各頂点ごとに、１番目と２番目に近いボーンに、より近い方に大きいウェイトが振られます。
　より具体的には、それぞれの距離をd1,d2として、
　　weight1 = (d2)/(d1+d2)
　　weight2 = (d1)/(d1+d2)
となります。

排他的：
　各頂点ごとに、最も近いボーンに全てのウェイトを設定します。

ボーンの座標と接続先などはあらかじめ設定しておいて下さい。また、接続先のないボーンにはウェイトが設定されません。



▼▼▼▼　つくったひと　▼▼▼▼

　　ｋｅｔ．(http://twitter.com/#!/k_e_t_)
バグとかなんかあったら言って下さい。


▼▼▼▼　免責事項　▼▼▼▼

ご利用は自己責任でっ！


▼▼▼▼　バージョン情報　▼▼▼▼

ver1.00 13/08/06
