# Position

PositionプロパティはVector・Number・Objectを許容します。

デフォルト値は `x=0, y=0, z=0` です。

```text
position: 3
// は以下のように解釈される
position: [3, 3, 3]
```

{% code title="position.oml" %}
```text
export default {
    component : "@cube",
    // 配列で表記する場合、配列の長さは3でなくてはいけない
    // ex) position : [1,1]   -> x
    //     position : [1,1,1] -> o
    position : [1,1,1],
    position : {
        x : 1, // x座標を設定する
        y : 1, // y座標を設定する
        z : 1  // z座標を設定する
        // オブジェクトで表記する場合, xyzはそれぞれ省略できる
        // ex) position : { x : 1, y : 1 }
    },
    rotation : [0,90,180],
    scale : [1,0.5,2]
}
```
{% endcode %}

