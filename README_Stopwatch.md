# ストップウォッチ
## メソッド
- 処理のまとまりのことをメソッドと呼びます。今まで出てきたものだと、カウントのアプリ`plus`や`minus`もメソッドだよ。
- 書き方

```swift
func メソッドの名前() {

}
```

例. 変数`label`の文字の色をコンソールに表示させるメソッド

```swift
func outputColor {
  print(label.textColor)
}
```

## タイマー
- **指定した時間に決まった動作を行うことができる**ものだよ！

- 書き方

```swift
var timer = Timer.scheduledTimer(
            timeInterval: 呼び出す間隔,
            target: self,
            selector: #selector(self.関数名),
            userInfo: nil,
            repeats: true または false
            )
```

- タイマーの止め方

```swift
timer.invalidate()
```

- タイマーが動いているかの確認

```swift
timer.isValid
```

## 否定の`!`

プログラミングでは、≠の代わりに!で否定を表します。  
例
```swift
if number != 9 {
  print("9ではないよ")
}
```

今回は、`timer.isValid`の左に!がついてるね。否定の`!`はつける位置が決まっていて、否定にしたいものの**左側**につけるよ。
