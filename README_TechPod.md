# テックポッド
## ここだけは抑えたい
- `UITableView`  
よくSNSでみられるタイムラインなどに使用されるよ！  
同じ見た目をしたものを並べる時に役立つよ！

- デリゲート  
`デリゲート`(移譲)というのは、`swift`の場合だと**他のクラスに頼みごとをする**という意味です。  
例えば、`UITableView`で`cell`を生成するメソッドは本来`UIViewController`クラスではすることができません。クラスにはできることとできないことがあります。ちゃんと一つ一つのクラスには役割があるからです。そこで自分以外の人にその人の得意分野を頼むことがあります。それをデリゲートと呼びます。  
デリゲートには、`UITableViewDelegate`や`UIImagePickerDelegate`(前回出てきたね！)などがあるよ。
- データソース  
デリゲートと同じ`プロトコル`という種類のものだよ。

- `UITableView`の使い方
  - 宣言
```swift
@IBOutlet var table: UITableView! //宣言
```
  - デリゲート/データソースを指定。
  ```
  table.delegate = self
  table.dataSource = self
  ```

  - デリゲートメソッドを使う。(その1)
  ```
  // このメソッドは何個のセルを表示するかを決めるメソッドだよ。
  func tableView(_ tableView: UITableView, numberOfRowsInSection section: Int) -> Int {

        return 10 //表示したいセルの個数をここに書こう。
    }
  ```

  - デリゲートメソッドを使う。(その2)
  ```swift
  // セルにデータを与えてあげることができるメソッド。
  func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {

        //セルの生成。
        let cell = tableView.dequeueReusableCell(withIdentifier: "Cell")

        cell?.textLabel?.text = "テスト" //ここでデータを与えている。

        return cell!
}
  ```
