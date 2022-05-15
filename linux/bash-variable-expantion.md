# bashの便利な変数展開

あることを知っているだけでシェルスクリプト書く時に効いてきそう。

```bash
$ v="hoge"
$ echo ${v:0:1}
h
$ echo ${v:2:2}
ge
$ echo ${v/e/u}
hogu
```
