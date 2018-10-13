# ストップウォッチ
## ここだけは抑えたい
- メソッド
    - 処理のまとまりのことをメソッドと呼びます。今まで出てきたものだと、ガチャアプリで出てきた`dismiss`もメソッドだよ！
    - 書き方
```swift
func メソッドの名前() {

}
```
例
```swift
func outputColor {

print(label.textColor)

}
```

- タイマー
    - 目覚ましのタイマーみたいに決まった時間になったら指定したメソッドを呼ぶことができるもの！
    - 書き方
    
```swift
let timer = Timer.scheduledTimer(
timeInterval: 呼び出す間隔,
target: self,
selector: #selector(self.関数名),
userInfo: nil,
repeats: true または false
)
```
   - 使い方
      - タイマーの止め方
`timer.invalidate()`
      - タイマーが動いているかの確認
`timer.isValid`


### この下は余裕があれば覚えていこう！

## 否定の`!`
プログラミングでは、≠の代わりに!で否定を表します。
例
```swift
if number == 9 {

print("9だよ")

}
```
```swift
if number != 9 {

print("9ではないよ")

}
```

今回は、`timer.isValid`の左に!がついてるね。否定の`!`はつける位置が決まっていて、否定にしたいものの左側につけるよ。

### なかなかのむずさやで。。(下) 

## `String`の`format`って？

ここを読んでる君は相当すごい。そんな君はおそらく下のコードが読めるだろう。

`label.text = String(number)`

ここでは数字を文字として表示している。この時にもし1が`number`に入っていたとしよう。つまり
```swift
print(label.text) // 1
```

しかし、ストップウォッチでは**1ではなく1.00と表示したい。** そんな時に、この`format`を用いる。色々なformat(書式)があるが、例えば、01と表記したい場合は、
```swift
label.text = String(format: "%02d", number) // 01
```
という風に書く。他にも色々あるので興味がある人はぜひ、[【Swift入門】数値を文字列(String)にformatする方法 | 侍エンジニア塾ブログ | プログラミング入門者向け学習情報サイト](https://www.sejuku.net/blog/34872)
を見てみてほしい！


