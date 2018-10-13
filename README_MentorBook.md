# メンターブック
# ここだけは抑えたい。
## クラス
- クラスとは一言で言うと設計図。プロパティとメソッドによって構成される。例えば、車のクラス(設計図)を作ります。
```swift
class Car {

  //車の車種
  var name: String!
  
  //ガソリンの量
  var gasolineMeter: Int!
  
  //車の値段
  var price: Int!

  .
  .
  .(省略)
  .
  .

  //運転できるかどうかのメソッド
  func canDrive() -> Bool {
    
    //運転時にガソリンの量を減らす。
    gasolineMeter -= 10
    
    //ガソリンがなくなったら。。。
    if gasolineMeter <= 0 {
    
      //false...偽りの -> 運転できない
      return false
    
    }else {
    
      true...真の -> 運転できる
      return true
    
    }
    
  }

}
```
