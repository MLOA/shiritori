# gitメモというか手作りチートシート
ローカルからディレクトリ作ってあげる方法があるけど
 向こうでディレクトリ及びURL発行してからやるのを想定

## URLをコピーしたのちcloneをする

$ git clone http://~~~~/user/hoge (作成するディレクトリ)

 ちなみにURLの後ろにディレクトリ名を指定できる
 これで自分のＰＣの中に複製される

## フォークリポジトリを作成する
 originがオンライン上の大元のリポジトリを指していて、ローカルから更新を加えていく
 逆に言うと元に戻したい場合に困ってしまう　
 そこでupstreamと呼ばれる別のリモートを作成しておくと便利な場合がある

$ git remote add upstream http://~~~~/user/hoge

## ブランチを作成して切り替えする

	$ git checkout -b (ブランチ名)

## ブランチを切り替える

	$ git checkout (ブランチ名)

## 自分のブランチをoriginへプッシュするときのながれ
 まずは大元(origin)のリモート指定

	$ git remote add origin http://~~~~/user/hoge

 コミットさせるファイルの指定

	$ git add (ファイル名)

 ディレクトリ内全て送るなら

	$ git add .

 コミットの記述をする

	$ git commit -m '記述する内容'

 プッシュする

	$git push origin (ブランチの指定)

## 更新した点を取得する

	$ git pull (ブランチ名)

 例えばoriginを取得するなら

	$ git pull origin

 fetch・mergeでやる方法もあるよ