# ガチャアプリ
## これだけは抑えよう。
- 乱数...指定した範囲の中でランダムに生成された数字。
- ファイルを追加する際に
- [x] Copy item if needed にチェックを入れる！
- 1つの`swift`ファイルに1つの画面が基本！
- コードと画面は違う世界。繋げることを忘れずに。
## 乱数
乱数の使い方
```swift
var number: Int = Int(arc4random_uniform(最大値))
```
## `UIImageView`の画像の設定
コードで書くと
```swift
monsterImageView(宣言した変数名).image = UIImage(named: "monster001")
```
## Segue
画面遷移(アプリで画面が切り替わること)をするときに**どの画面からどの画面へ移るのかを決めるために使用する。**
