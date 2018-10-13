# メモ帳
## ここだけは抑えたい。

### .swiftファイルの作成方法
- ViewControllerのファイルを作る時
  - `Cocoa Touch Class`を選択しよう
- オリジナルのクラスを作る時
  - `Swift File`を選択しよう

### UserDefaults
一言で言うとデータの保存を行うためのもの。特にユーザーが自分で入力したデータを保存したりするよ。情報の倉庫(データベース)と呼ばれてるよ。

**UserDefaultsの使い方3ステップ**

  1. データベースを作る(UserDefaultsを宣言する)
  2. データベースに値を保存する。
  3. データベースの値を取り出す。

- データベースの作り方
```swift
let database: UserDefaults = UserDefaults.standard
```
- データベースに値を保存する方法
```swift
database.set(保存したい値, forKey: "鍵(パスワード)")
```

- データベースの値を取り出す方法
```swift
変数 = database.object(forKey: "鍵(パスワード)")
```
### アラート
アラートの使い方3ステップ
1. アラートを作る
2. ボタンを作る
3. アラートを表示させる

- アラートの作り方
```swift
let alert = UIAlertController(title: "タイトル", message: "本文", preferredStyle: .alert)
```

- ボタンを作る
```swift
alert.addAction(UIAlertAction(
  title: "",
  style: .default,
  handler: nil
  ))
```

- アラートを表示させる
```swift
present(alert, animated: true, completion: nil)
```
