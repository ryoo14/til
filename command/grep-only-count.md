# grepで検索結果に一致する件数を出力する

`-c`オプションを付与すると検索結果に一致する件数だけ出力できる。

```bash
$ cat hoge.txt 
aaa
bbb
ccc
$ grep -c 'aaa' hoge.txt
1
```
