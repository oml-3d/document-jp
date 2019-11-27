# Registered 3D models

OMLは下記のいくつかの3Dオブジェクトがデフォルトで定義されています。

* cube
* cylinder
* sphere
* capsule

各オブジェクトを宣言する際、オブジェクトは@（アットマーク）の書き出しから始まり、`" "` （ダブルクオーテーション）もしくは `' '` （シングルクオーテーション）で囲われている必要があります。

{% code title="sample" %}
```text
component : "@cube",
component : "@cylinder",
component : "@sphere",
component : "@capsule
```
{% endcode %}

{% code title="cube.oml" %}
```text
export default {
    component : "@cube"
}
```
{% endcode %}

各オブジェクトに対してグループ化やプロパティを適用することで様々な設定をすることができます。詳細は下記のリンク先をご参照ください。

{% page-ref page="../properties/position.md" %}

{% page-ref page="../properties/color.md" %}

{% page-ref page="../properties/texture.md" %}

{% page-ref page="../properties/sound.md" %}



