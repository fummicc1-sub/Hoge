# メンターブック

# クラス
クラスとは一言で言うと**設計図**。プロパティとメソッドによって構成される。

# プロパティ
プロパティとはクラスの特徴を表したものだよ。例えば、人だったら名前や年齢など**その人の部品となるもの**みたいなイメージだよ。

# メソッド
前回の教科書で出てきたね。これは同じ処理を何回も色々な場所で使う場合に使用していたね。このメソッドも人で例えてみると、歩く動作や寝る動作などのことを言うよ。

# インスタンス
**クラス**は設計図なので**目にみえません。** なので、目に見えるようにしてあげる必要があります。それが**インスタンス化**です。

車のクラス(設計図)を例にしてみます。
```swift
class Car {
  var color: UIColor = UIColor.black
}

let redCar: Car = Car() //インスタンス化
redCar.color = UIColor.red

let blueCar: Car = Car() //インスタンス化
blueCar.color = UIColor.blue
```

# 引数と戻り値
```swift
func kaimono(price1: Int, price2: Int) -> Int {
  let cost = price1 + price2
  return cost
}
```

上の場合でいう、`price1`と`price2`が引数, `return cost`が戻り値です。ここではこれ以上深入りしませんが気になったら検索してみて！
