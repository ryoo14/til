# 外部の設定ファイルを読み込む

iniファイルのような外部の設定ファイルを読み込む方法

例えばこんなiniファイルがあるとする

```ini
[config]
a = hoge
b = fuga
```

こう書ける

```go
import "gopkg.in/ini.v1"

func main() {
  config, err := ini.Load("config.ini")
  if err != nil {
    a := ini.Section("config").Key("a").String()
    b := ini.Section("config").Key("b").String()
  }
}
```

YAMLファイルの読み込み方がすごいややこしい方法しかでてこなかった…
