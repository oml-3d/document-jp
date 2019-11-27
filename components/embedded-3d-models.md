# Embedded 3D models

`@model` コンポーネントを使用することで、ユーザーが用意した任意の3Dオブジェクトを読み込ませることができます。

モデルの読み込みは絶対パスと相対パス双方の指定方法に対応しています。リンク先は `( )` （パーレン・丸括弧）で囲って表記してください。

```text
component : "@model(https://sample.com/sample.fbx)"
component : "@model(./sample.fbx)"
```

{% code title="embedded-model.oml" %}
```text
export default {
    component : "@model(https://sample.com/sample.fbx)"
}
```
{% endcode %}

対応している3Dモデルの拡張子は以下の通りです。

|  |  |  |  |
| :---: | :---: | :---: | :---: |
| 3D | 3DS | 3MF | AC |
| AC3D | ACC | AMF | AMJ |
| ASE | ASK | B3D | BLEND |
| BVH | COB | DAE/Collada | DXF |
| ENFF | FBX | glTF 1.0 + GLB | glTF 2.0 |
| IFC-STEP | IRR / IRRMESH | LWO | LWS |
| LXO | MD2 | MD3 | MD5 |
| MDC | MDL | MESH/MESH.XML | MOT |
| MS3D | NDO | NFF | OBJ |
| OFF | OGEX | PLY | PMX |
| PRJ | Q3O | Q3S | RAW |
| SCN | SIB | SMD | STL |
| TER | UC | VTA | X |
| X3D | XGL | ZGL |  |

グループ化やプロパティを適用することで様々な設定をすることができます。詳細は下記のリンク先をご参照ください。

{% hint style="info" %}
3Dモデルにすでにテクスチャとして色が反映されている場合、colorプロパティは乗算されて描画されます。
{% endhint %}

{% page-ref page="group.md" %}

{% page-ref page="../properties/position.md" %}

{% page-ref page="../properties/rotation.md" %}

{% page-ref page="../properties/scale.md" %}

{% page-ref page="../properties/color.md" %}

{% page-ref page="../properties/texture.md" %}

{% page-ref page="../properties/sound.md" %}

## 

![https://github.com/oml-3d/document-jp/components/embedded-3d-models.md](../.gitbook/assets/github-mark-32px.png)

