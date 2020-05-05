# AAR Shinkan2020 Webページ
AARの新歓ページ2020年版です．いろんな人に記事を書いてもらう関係でこんな感じになってます(雑)

## gitの使い方
最低限使うやつだけ
エラーが出たらググってください

### このプロジェクトをダウンロードする
Macでの例です
```sh
cd (作業用のフォルダ)
git clone https://github.com/auxa-m45/Shinkan2020.git
```

### 編集したあとアップロードする
* `git add -A`
    プロジェクト内の全部のファイルをステージ(アップロードする変更をまとめておくところ)に登録する

* `git commit -m "変更内容を簡潔に"`
    ステージに登録されている変更を"変更内容を〜"というメッセージとともにコミットする
* `git push origin master`
    手元のコミットをpush(サーバーにアップロード)する

```sh
git add -A
git commit -m "変更内容を簡潔に"
git push origin master
```

## うごかしかた
hugoという静的サイトジェネレーターを使っています
#### 1. hugoをインストール（Mac）
```sh
brew install hugo
```

#### 2. 動かしてみる
下書きモードで動かします
```
hugo serve -D
```

#### 3. 見てみる
たぶん[localhost:1313](http://localhost:1313)をブラウザで開くと見られるようになっているはず．ちなみにエディタでファイルをいじって保存すると自動的に反映されます．すごいね

### 5/6 追加(naya-sync)
忘れないように勝手ながら…
ブランチで作業
```
git checkout (自分のブランチ)
git fetch
git merge origin/master
```
