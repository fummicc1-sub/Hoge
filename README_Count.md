# カウントアプリ

# これだけは抑えよう。
- `ViewController.swift`...コードを書くところ。
- `Main.storyboard`...アプリの見た目を整えるところ。
- 変数の宣言の仕方
  - `var` `変数名` `:` `型名` `=` `最初のデータ`
    - `var number: Int = 0`
    
---

## Xcodeの使い方
- `ViewController.swift`...コードを書くところ。
- `Main.storyboard`...アプリの見た目を整えるところ。

## プログラミングの基礎
- 変数...データを入れておく箱。
- 型...変数のデータの種類。
- 関数...処理のまとまり。
- 宣言...変数や関数を使うための手続き。


## プログラミングの書き方(構文)
- 変数の宣言の仕方
  - `var` `変数名` `:` `型名` `=` `最初のデータ`
    - var number: Int = 0

-  `if`文
  - 「もし〇〇があったら〜」という意味。
  - 例. もし数字が10以上だったら、文字を赤くする。
  
  ```
  if (条件: 数字が10以上) {
    
    (処理の内容: 文字を赤くする)
    
  }
```

  ↓
  
```
  if (number >= 10) {
  
    label.textColor = UIColor.red
  
  }
  ```
  
