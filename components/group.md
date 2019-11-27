# Group

groupコンポーネントでは内部に配列の形でコンポーネントを定義することにより、一つのオブジェクトとして振る舞わせることができます。

{% code title="group.oml" %}
```text
export default {
    group : [{
        component : "@cube",
        position : [1,1,1] 
    },{
        component : "@sphere",
        position : [2,2,2]
    }]
}
```
{% endcode %}

OMLでは親子構造を採用しているため、以下のような親子関係とプロパティの設定がなされている場合、group2.oml のように表記されます。

group内のコンポーネントのプロパティは親からの相対値で定義されます。

```text
groupA
    ∟groupB
        ∟component1
        ∟component2
    ∟groupC
        ∟component3
        ∟component4
```

{% code title="group2.oml" %}
```text
export default {
    group : [{
        group : [{
            component : "@cube",
            position : [1,1,1] 
        },{
            component : "@sphere",
            position : [3,3,3]
        }],
        position : [1,1,1]
    },{
        group : [{
            component : "@cube",
            position : [1,1,1] 
        },{
            component : "@sphere",
            position : [3,3,3]
        }],
        position : [5,5,5]
    }]
}
```
{% endcode %}

{% page-ref page="../properties/position.md" %}

{% page-ref page="../properties/rotation.md" %}

{% page-ref page="../properties/scale.md" %}

{% page-ref page="../properties/color.md" %}

{% page-ref page="../properties/texture.md" %}

{% page-ref page="../properties/sound.md" %}

## 

![https://github.com/oml-3d/document-jp/components/group.md](../.gitbook/assets/github-mark-32px.png)

