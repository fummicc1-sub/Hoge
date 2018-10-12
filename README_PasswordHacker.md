# パスワードハッカー
## ここだけは抑えよう。
### ループ文
ループ文とは、同じ処理を繰り返して行うことができる構文。2種類ある。

- `for`文

```swift
for i in 0..<10 {
  print(i) 
}
```
```
0
1
2
3
4
5
6
7
8
9
```

- `while`文
```swift
var number: Int = 0

while number < 10 {

  print(number)  
  number = number + 1
  
}
```
```
0
1
2
3
4
5
6
7
8
9
```

### 処理を〇〇秒送らせる(待機させる)方法
```swift
RunLoop.main.run(until: Date(timeIntervalSinceNow: 〇〇))
```
