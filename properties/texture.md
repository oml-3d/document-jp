# Texture

Textureプロパティでは、ユーザーの定義する画像が主に3Dコンポーネントに対して全部の面に繰り返し適用されます。

画像の適用は絶対パスと相対パス双方の指定方法に対応しています。リンク先は `" "` （ダブルクオーテーション）もしくは `' '` （シングルクオーテーション）で囲われている必要があります。

```text
texture : "https://sample.com/sample.jpg"
texture : "./sample.jpg"
```

```text
export default {
    component : "@cube",
    texture : "https://sample.com/sample.jpg"
    // cubeの全６面に同じ画像が適用される
}
```

対応している画像の拡張子は以下の通りです。

|  |  |
| :--- | :--- |
|  |  |

