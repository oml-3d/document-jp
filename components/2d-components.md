# 2D components

OMLにはいくつかの2Dコンポーネントが標準で定義されています。

* plane
* image/video
* text

各コンポーネントを宣言する際、オブジェクトは@（アットマーク）の書き出しから始まり、`" "` （ダブルクオーテーション）もしくは `' '` （シングルクオーテーション）で囲われている必要があります。

## Plane

{% code title="plane.oml" %}
```text
export default {
    component : "@plane"
}
```
{% endcode %}

rotationが宣言されていない場合、planeはxz面に対して垂直に表示されます。

表面のみ描画されます。

## Image / Video

`@image` `@video`コンポーネントを使用することで、ユーザーが用意した任意の画像データ、映像データを読み込ませることができます。

画像データ、映像データの読み込みは絶対パスと相対パス双方の指定方法に対応しています。リンク先は `( )` （パーレン・丸括弧）で囲って表記してください。

```text
component : "@image(https://sample.com/sample.jpg)"
component : "@video(./sample.mp4)"
```

{% code title="image.oml" %}
```text
export default {
    component : "@image(https://sample.com/sample.jpg)"
}
```
{% endcode %}

{% hint style="info" %}
OML ver 0.2.1 betaでは 映像ファイル操作プロパティは定義されていません。映像データはループ再生されます。
{% endhint %}

対応している画像ファイル及び映像ファイルの拡張子は以下の通りです。

| 画像 | 映像 |
| :---: | :---: |
| .jpg | .dv |
| .png | .m4v |
| .tga | .mov |
| .bmp | .mp4 |
| .psd | .mpg |
| .gif | .mpeg |
| .hdr | .ogv |
| .pic | .vp8 |
| .pnm | .webm |



## Text

Textコンポーネントではユーザーが指定する任意の文字列を表示させることができます。

文字列は `( )` （パーレン・丸括弧）で囲って表記してください。

{% hint style="info" %}
OML ver 0.2.1 betaでは、フォント指定プロパティ及び操作プロパティが定義されていません。デフォルトフォントは[Noto Sans](https://www.google.com/get/noto/) Regularで、中央揃えで表示されます。
{% endhint %}

{% code title="text.oml" %}
```text
export default {
    component : "@text(サンプルテキストです。)"
}
```
{% endcode %}

rotationが宣言されていない場合、textはxz面に対して垂直に表示されます。

なお、`\n`で改行することができます。

{% code title="indention.oml" %}
```text
export default {
    component : "@text(これは\nサンプルテキストです。)"
}
```
{% endcode %}



グループ化やプロパティを適用することで様々な設定をすることができます。詳細は下記のリンク先をご参照ください。

{% page-ref page="group.md" %}

{% page-ref page="../properties/position.md" %}

{% page-ref page="../properties/rotation.md" %}

{% page-ref page="../properties/scale.md" %}

{% page-ref page="../properties/color.md" %}

{% page-ref page="../properties/texture.md" %}

{% page-ref page="../properties/sound.md" %}

