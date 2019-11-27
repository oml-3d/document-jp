# Scale

ScaleプロパティはVector・Number・Objectを許容します。

デフォルト値は `x=1, y=1, z=1` です。

```text
scale : 2
// は以下のように解釈される
scale : [2, 2, 2]
```

{% code title="scale.oml" %}
```text
export default {
    component : "@cube",
    // 配列で表記する場合、配列の長さは3でなくてはいけない
    // ex) scale : [2,2]   -> x
    //     scale : [2,2,2] -> o
    scale : [2,2,2],
    scale : {
        x : 2, // x軸を中心にした回転を設定する
        y : 2, // y軸を中心にした回転を設定する
        z : 2  // z軸を中心にした回転を設定する
        // オブジェクトで表記する場合, xyzはそれぞれ省略できる
        // ex) scale : { x : 2, y : 2 }
    },
    position : [1,1,1],
    rotation : [90,180,0]
}
```
{% endcode %}

