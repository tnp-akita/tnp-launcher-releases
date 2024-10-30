# tnp-launcher-releases

tnp-launcherのゲームを管理するためのリポジトリです。

## ゲームの追加方法

1. **Releases ページに移動する**
2. **tnp-launcher で一意のゲームを表すタグを作成する**
   - **必ず `snake_case` で記述してください**
   - ここで入力した内容が、tnp-launcher 内でのゲームの管理IDになります
   - 例: `corelynx`, `type_beat`, `isu_golf`
3. **`Release title` にゲームの名前を入力する**
   - ここで入力した名前が、ゲーム名として表示されます
4. **`Describe this release` にゲームの説明文を入力する**
   - ここで入力した説明が、ゲームの説明文として表示されます
   - 以下を必ず記述してください

自分の内容に変更した上で、一番最初に記述してください

| キー         | 値                             |
|-------------|--------------------------------|
| `creator`   | 作者の名前を記述                  |
| `comment`   | ゲームの一覧に表示される一言コメント |

```md
---
creator: 空中ブランコ
comment: 椅子でゴルフをしよう!
---
```

内容に以下のものを含めてください
    
| 見出し       | 内容                      |
|-------------|--------------------------|
| **変更履歴** | バージョンごとの変更履歴を記述 |

**例**

```md
---
creator: 空中ブランコ
comment: 椅子でゴルフをしよう!
---

# イスゴルフの世界へ・・・

突如、オフィス内で起きた珍事件「**イスゴルフ**」

上司がいないことをいいことに、オフィスで遊んでいたところ、ある一人が

（省略）

## 変更履歴

| バージョン   | 変更内容                                |
|------------|----------------------------------------|
| `v1.0.2`   | 名前が反映されなくなる問題を解決            |
| `v1.0.1`   | 2プレイ目以降リセットされない問題を解決      |
| `v1.0.0`   | リリース                                |
```

5. **`icon.png` をアップロードする**
   - アップロードした画像がゲームのアイコンとして表示されます
6. **`thumbnail-*.png` をアップロードする**
   - アップロードした画像がゲームのサムネイルとして表示されます
   - `*` の部分は任意に変更可能です
   - `thumbnail-` から始まり `.png` で終わるファイルを検索して表示します
   - ファイル名順にソートされます
7. **ゲームファイルを zip 形式でアップロードする**
   - 必ず zip ファイル形式でアップロードしてください
   - zip ファイルの階層は以下を参考にしてください
```
IsuGolf-1.0.0.zip
├── manifest.json
|  (以下ゲームファイル)
├── IsuGolf_Data/
├── IsuGolf.exe
├── MonoBleedingEdge/
├── UnityCrashHandler64.exe
└── UnityPlayer.dll
```
   - zip ファイルに `manifest.json` を含め、以下の内容を参考に作成してください:

| キー        | 値                  |
|------------|---------------------|
| `execFilePath` | 実行ファイルのパス     |

```json
{
  "execFilePath": "IsuGolf.exe"
}
```

   - **ファイル名は `ゲーム名-バージョン.zip` の形式で作成してください**
     - 例: `Corelynx-1.0.0.zip`, `TypeBeat-1.2.1.zip`
     - ファイル名の最後の `-` から `.zip` までの部分でバージョンを認識します
     - **バージョンにはハイフンを含めないでください** (例: `v-1.0.0` は不可)
8. **`Publish release` を押す**

---

## ゲームの更新方法

1. **Releases ページに移動する**
2. **対象ゲームのリリース右上にある `Edit` を押す**
3. **`Describe this release` に変更履歴を追記する**
4. **更新したゲームファイルを zip 形式でアップロードする**
  - zip ファイルの階層は以下を参考にしてください
```
IsuGolf-1.0.0.zip
├── manifest.json
|  (以下ゲームファイル)
├── IsuGolf_Data/
├── IsuGolf.exe
├── MonoBleedingEdge/
├── UnityCrashHandler64.exe
└── UnityPlayer.dll
```
   - zip ファイルに `manifest.json` を含め、以下の内容を参考に作成してください:

| Key        | Value               |
|------------|---------------------|
| `execFilePath` | 実行ファイルのパス |

```json
{
  "execFilePath": "IsuGolf.exe"
}
```

   - **ファイル名は `ゲーム名-バージョン.zip` の形式で作成してください**
     - 例: `Corelynx-1.0.0.zip`, `TypeBeat-1.2.1.zip`
     - ファイル名の最後の `-` から `.zip` までの部分でバージョンを認識します
     - **バージョンにはハイフンを含めないでください** (例: `v-1.0.0` は不可)
5. **`Update release` を押す**
