# Ruby on Rails チュートリアルのサンプルアプリケーション(docker設定付き)

これは、次の教材で第５章までやった時のソースコードです。
[*Ruby on Rails チュートリアル: 実例を使って Rails を学ぼう*](http://railstutorial.jp/)
[Michael Hartl](http://www.michaelhartl.com/) 著
また、docker上で動かすための設定ファイル（Dockerfile, docker-compose.yml）が含まれています。

## ライセンス

[Ruby on Rails チュートリアル](http://railstutorial.jp/)内にあるすべてのソースコードは
MIT ライセンスと Beerware ライセンスのもとに公開されています。
詳細は [LICENSE.md](LICENSE.md) をご覧ください。

まずはこのファイルをクローンしてして、そのあと次のように実行しましょう。
1. パスワードファイルを追加する
  * .envファイルを作ってパスワードを追加しよう
2. dockerの環境をbuildする

```
   % docker-compose build
```

3. railsコンテナで関連ライブラリ等をインストールする

```
   % docker-compose run --rm web bundle install
```

4. データベースを作る

```
   % docker-compose run --rm web rails db:create
   % docker-compose run --rm web rails db:migrate
```

5. railsサーバを立ち上げる

```
   % docker-compose up
```
