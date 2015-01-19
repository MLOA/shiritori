# gitメモというか手作りチートシート
 ローカルからディレクトリ作ってあげる方法があるけど

 向こうでディレクトリ及びURL発行してからやるのを想定

 __よく使うだろうコマンドをべべべと記述します__

 結構乱暴な書き方です。すいません

### URLをコピーしたのちcloneをする

	$ git clone http://~~~~/user/hoge (作成するディレクトリ)

 ちなみにURLの後ろにディレクトリ名を指定できる

 これで自分のＰＣの中に複製される

### フォークリポジトリを作成する
 originがオンライン上の大元のリポジトリを指していて、ローカルから更新を加えていく

 逆に言うと元に戻したい場合に困ってしまう
　
 そこでupstreamと呼ばれる別のリモートを作成しておくと便利な場合がある

	$ git remote add upstream http://~~~~/user/hoge

### ブランチを作成して切り替えする

	$ git checkout -b (ブランチ名)

### ブランチを切り替える

	$ git checkout (ブランチ名)

### 自分のmasterブランチをoriginへプッシュするときのながれ
	$ git checkout master

 まずは大元(origin)のリモート指定

	$ git remote add origin http://~~~~/user/hoge

 コミットさせるファイルの指定

	$ git add (ファイル名)

 ディレクトリ内全て送るなら

	$ git add .

 コミットの記述をする

	$ git commit -m '記述する内容'

 プッシュする

	$ git push origin (ブランチの指定)

### 自分が作成したブランチからpushするとき
 初めてプッシュするときに

	$ git push --set-upstream origin (ブランチ名)

 次からは--set-upstreamは省ける？

### 更新した点を取得する

	$ git pull (リポジトリ)

 例えばoriginを取得するなら

	$ git pull origin

 fetch・mergeでやる方法もあるよ
　
 とりあえず変更点を取得だけする

	$ git fetch (リポジトリ名)

 変更を反映させる

	$ git merge (リポジトリ名)/(反映させたいブランチ)
