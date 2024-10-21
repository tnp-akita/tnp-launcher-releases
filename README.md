# tnp-launcher-releases

tnp-launcherのゲームを管理するためのリポジトリです。

## How to add a game?

1. Releases ページに飛びます
2. tnp-launcherで一意のゲームを表すTagを作成します
  - **必ず`snake_case`で記述してください**
  - ここに入力した内容がtnp-launcher内のゲームの管理IDになります
  - (例) `corelynx` `type_beat` `isu_golf`
3. `Release title`にゲームの名前を入力します
  - ここに入力した内容がゲームの名前として表示されます
4. `Describe this release`にゲームの説明文を入力します
  - ここに入力した内容がゲームの説明文として表示されます
  - 以下の内容を必ず入力するようにしてください
    - 変更履歴
      - バージョンごとの変更履歴を入力してください
5. `Attach binaries by dropping them here or selecting them`に`icon.png`をアップロードします
  - アップロードした画像がゲームのアイコンとして表示されます
6. `Attach binaries by dropping them here or selecting them`に`thumbnail-*.png`をアップロードします
  - アップロードした画像がゲームのサムネイルとして表示されます
  - `*`の部分は任意で変更してください
  - `thumbnail-`から始まり`.png`で終わるファイルを対象に検索をかけています
  - ファイル名順にソートを行います
7. `Attach binaries by dropping them here or selecting them`に作成したゲームをアップロードします
  - 必ずzipファイルでアップロードしてください
  - ファイル名は`ゲーム名-バージョン.zip`のように記述してください
    - 最後の`-`から`.zip`までをバージョンとして認識します
    - そのため、バージョンをつける際はバージョン内にハイフンを入れないようにしてください
      - つまり`v-1.0.0`とかはダメです
    - (例) `Corelynx-1.0.0.zip` `TypeBeat-1.2.1.zip`
8. `Publish release`を押します

## How to update a game?

1. Releases ページに飛びます
2. 対象のゲームのReleaseの右上にある`Edit`を押します
3. `Describe this release`の変更履歴を追記します
4. `Attach binaries by dropping them here or selecting them`にアップデートしたゲームをアップロードします
  - ゲームのバージョンはアップロードした順番にソートされます
  - 必ずzipファイルでアップロードしてください
  - ファイル名は`ゲーム名-バージョン.zip`のように記述してください
    - 最後の`-`から`.zip`までをバージョンとして認識します
    - そのため、バージョンをつける際はバージョン内にハイフンを入れないようにしてください
      - つまり`v-1.0.0`とかはダメです
    - (例) `Corelynx-1.0.0.zip` `TypeBeat-1.2.1.zip`
5. `Update release`を押します
