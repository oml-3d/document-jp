# onClick

指を触れたオブジェクトと指を離したオブジェクトが同一のときに発火するイベントです。

イベントが発火したオブジェクトを含めて、その親をたどるように他のオブジェクトに関してイベントが発火します。 

以下の親子構造があるとする場合、EEEでonClickによるイベントが感知されると`EEE,CCC,BBB,AAA`が含む全てのonClickイベントが発火され、 `DDD`でイベントが感知されると`DDD,BBB,AAA`が含む全てのonClickイベントが発火されます。

```text
AAA
 └BBB
   └CCC
     └EEE
   └DDD
```

{% code title="change\_color.oml" %}
```text
export default {
    component : "@cube",
    color : "#FF0000",
    onClick : function() {
        // 押されたら赤色から青色に変わる
        this.color = "#0000FF";
    }
}
```
{% endcode %}

