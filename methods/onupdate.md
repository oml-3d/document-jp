# onUpdate

１秒間に約60回呼ばれるイベントです。

{% code title="move.oml" %}
```text
export default {
    component : "@cube",
    position : [0,0,0],
    onUpdate : function() {
        // 1フレームに0.1ずつx方向に移動します
        this.position.x += 0.1;
    }
}
```
{% endcode %}

