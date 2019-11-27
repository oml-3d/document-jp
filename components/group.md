# Group

groupコンポーネントでは内部に配列の形でコンポーネントを定義することにより、一つのオブジェクトとして振る舞わせることができます。

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





