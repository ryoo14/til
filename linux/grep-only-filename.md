# grepで検索結果に一致するファイル名だけ出力する

`-l`オプションを付与すると検索結果に一致するファイル名だけ出力できる。

```bash
$ cat hoge.txt 
aaa
bbb
ccc
$ grep 'aaa' *
hoge.txt:aaa
$ grep -l 'aaa' *
hoge.txt
```
