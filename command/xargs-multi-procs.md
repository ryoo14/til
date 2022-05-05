# xargsで並列実行する

`-P`オプションでコマンドを並列実行できる。

```bash
# 1コア使って実行
$ time seq 100000 | xargs -n1 touch

real	0m45.691s
user	0m27.478s
sys	0m19.395s

# 8コア使って並列実行
$ time seq 100000 | xargs -n8 touch

real	0m7.486s
user	0m3.621s
sys	0m3.994s
```
