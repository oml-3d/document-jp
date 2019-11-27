# Rotation

RotationプロパティはVector・Number・Objectを許容します。

オイラー角を使用してそれぞれの軸を中心にした回転角を入力します。

{% hint style="info" %}
x, y, zの角度は、z軸→ x軸→ y軸の順に回転します。
{% endhint %}

デフォルト値は `x=0, y=0, z=0` です。

```text
rotation : 90
// は以下のように解釈される
rotation : [90, 90, 90]
```

{% code title="rotation.oml" %}
```text
export default {
    component : "@cube",
    // 配列で表記する場合、配列の長さは3でなくてはいけない
    // ex) rotation : [90,90]   -> x
    //     rotation : [90,90,90] -> o
    rotation : [90,90,90],
    rotation : {
        x : 90, // x軸を中心にした回転(度)を設定する
        y : 90, // y軸を中心にした回転(度)を設定する
        z : 90  // z軸を中心にした回転(度)を設定する
        // オブジェクトで表記する場合, xyzはそれぞれ省略できる
        // ex) rotation : { x : 90, y : 90 }
    },
    position : [1,1,1],
    scale : [1,0.5,2]
}
```
{% endcode %}

