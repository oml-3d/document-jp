# Sound

Soundプロパティでは、ユーザーの定義する音声データがコンポーネントに対して適用されます。

音源は、適用されたコンポーネントの中心点に配置され、距離に応じて音量が変化します。

{% hint style="info" %}
OML ver 0.2.1 beta では音声ファイル操作プロパティが定義されていません。音声データはループ再生されます。
{% endhint %}

音声ファイルの適用は絶対パスと相対パス双方の指定方法に対応しています。リンク先は `" "` （ダブルクオーテーション）もしくは `' '` （シングルクオーテーション）で囲われている必要があります。

```text
sound : "https://sample.com/sample.mp3"
sound : "./sample.mp3"
```

{% code title="sound.oml" %}
```text
export default {
    component : "@cube",
    position : [1,1,1],
    scale : [1,1,1],
    sound : "https://sample.com/sample.mp3"
    // cubeの中心点である[1,1,1]に音源が配置される
}
```
{% endcode %}

また、空のコンポーネントに対して音源を適用することもできます。

{% code title="sound2.oml" %}
```text
export default {
    sound : "https://sample.com/sample.mp3"
    // positionが宣言されていないため、[0,0,0]に音源のみが配置される
}
```
{% endcode %}

対応している音声ファイルの拡張子は以下の通りです。

|  |  |  |
| :---: | :---: | :---: |
| .mp3 | .ogg | .wav |
| .aiff / .aif | .mod | .it |
| .s3m | .xm |  |



## 

![https://github.com/oml-3d/document-jp/properties/sound.md](../.gitbook/assets/github-mark-32px.png)

