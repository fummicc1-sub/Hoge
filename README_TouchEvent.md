# タッチイベント
## ここだけは抑えたい
### タッチイベント
画面をタッチしたら呼ばれるメソッド。
指の位置や動きを取得することができる。

- タッチ開始時に呼ばれるメソッド(タッチ)

```swift
override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {



}
```

- タッチを動かした時に呼ばれる。(ドラッグ)

```swift
override func touchesMoved(_ touches: Set<UITouch>, with event: UIEvent?) {



}
```

- タッチを話した時に呼ばれる。(タッチ・ドラッグ終了)

```swift
override func touchesEnded(_ touches: Set<UITouch>, with event: UIEvent?) {

}
```

- フォトアルバムを使用する。

  1. `Info.plist`で`Privacy - Photo Library Usage Description`を設定。
  2. フォトライブラリを使うコードを書く。(省略)
  3. アルバムの写真を選択したら、写真を取得する。
  4. 画面の写真(スクリーンショット)を保存する。
  ---
  - Step1... `Info.plist`ファイルを開いて設定しよう！
  - Step2

```swift
let imagePickerController: UIImagePickerController! //imagePickerの宣言

(省略)
.
.
.

func フォトライブラリを開こう() {
  imagePickerController.sourceType = UIImagePickerController.SourceType.photoLibrary
  imagePickerController.delegate = self
  imagePickerController.allowsEditing = true

  self.present(imagePickerController, animated: true, completion: nil)

}

```

  - Step3

```swift
  //写真をピッカーで選択したら自動的に呼ばれるメソッド
  func imagePickerController(_ picker: UIImagePickerController, didFinishPickingMediaWithInfo info: [UIImagePickerController.InfoKey : Any]) {

        //写真を取得
        let image = info[UIImagePickerController.InfoKey.originalImage] as! UIImage

        //写真を表示
        imageView.image = image

        //ピッカーを消去
        dismiss(animated: true, completion: nil)

  }
```

- Step4

```swift
UIGraphicsBeginImageContext(view.frame.size)

self.view.layer.render(in: UIGraphicsGetCurrentContext()!)

let capture = UIGraphicsGetImageFromCurrentImageContext()!

UIGraphicsEndImageContext()

UIImageWriteToSavedPhotosAlbum(capture, nil, nil, nil)
```
