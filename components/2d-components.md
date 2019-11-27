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

{% hint style="info" %}
OML ver 0.2.1 betaでは 映像ファイル操作プロパティは定義されていません。映像データはループ再生されます。
{% endhint %}

対応している画像ファイル及び映像ファイルの拡張子は以下の通りです。

## Text

Textコンポーネントではユーザーが指定する任意の文字列を表示させることができます。

文字列は `( )` （パーレン・丸括弧）で囲って表記してください。

{% hint style="info" %}
OML ver 0.2.1 betaでは、フォント指定プロパティ及び操作プロパティが定義されていません。デフォルトフォントは[Noto Sans](https://www.google.com/get/noto/) Regularで、中央揃えで表示されます。
{% endhint %}

```text
export default {
    component : "@text(サンプルテキストです。)"
}
```

rotationが宣言されていない場合、textはxz面に対して垂直に表示されます。

なお、`\n`で改行することができます。

```text
export default {
    component : "@text(これは\nサンプルテキストです。)"
}
```



グループ化やプロパティを適用することで様々な設定をすることができます。詳細は下記のリンク先をご参照ください。

{% page-ref page="../properties/position.md" %}

{% page-ref page="../properties/color.md" %}

{% page-ref page="../properties/texture.md" %}

{% page-ref page="../properties/sound.md" %}

## 

![https://github.com/oml-3d/document-jp/components/2d-components.md](../.gitbook/assets/github-mark-32px.png)

