# ファイル読み書きとClose不要な手法

## ファイル読み込み

```vb
Imports System.IO

Dim FileReader As StreamReader = StreamReader(FILEPATH)

' 全行読み込み
FileReader.ReadToEnd
' 1行読み込み
FileReader.ReadLine

' Close
FileReader.Close()
```
## ファイル書き込み

```vb
Imports System.IO

' 2つめの引数(Boolean)はTrueなら追記、Falseなら上書き
Dim FileWriter As StreamWriter = StreamWriter(FILEPATH, True)

' 改行なし書き込み
FileWriter.Write("Test")
' 改行あり書き込み
FileWriter.WriteLine("Test")

' Close
FileWriter.Close()
```

`Reader`にしても`Writer`にしてもOpenするからには`Close`するべきだが、`Using`句を使うと明示的に`Close`しなくても済む。

```vb
Using FileReader As New StreamReader(FILEPATH)
    FileReader.ReadToEnd
End Using
```
