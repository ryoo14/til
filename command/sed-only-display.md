# sedで処理した行のみ表示する

`-n`オプションと`p`コマンドでできる。

```bash
$ cat hoge.txt
a
b
c

$ sed '/a/p' hoge.txt
a
a
b
c

$ sed -n '/a/p' hoge.txt                                                                                                                                                         
a
```
