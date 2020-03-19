# CPUなどの情報をコマンドで取得する

Macには`/proc`がないため、`cpuinfo`からCPU情報を確認したりすることができない。

代わりに`system_profiler SPHardwareDataType`というコマンドが使える。

```sh
$ system_profiler SPHardwareDataType
Hardware:

    Hardware Overview:

      Model Name: MacBook
      Model Identifier: MacBook10,1
      Processor Name: Dual-Core Intel Core m3
      Processor Speed: 1.2 GHz
      Number of Processors: 1
      Total Number of Cores: 2
      L2 Cache (per Core): 256 KB
      L3 Cache: 4 MB
      Hyper-Threading Technology: Enabled
      Memory: 8 GB
      Boot ROM Version: 184.0.0.0.0
      SMC Version (system): 2.42f12
      Serial Number (system): C02YJ1NUHH21
      Hardware UUID: EF99C1BA-CCE6-5C86-9FE0-F2FA9DF4E4EF
```

CPU情報以外にも色々取れるらしく、`-listDataTypes`オプションをつけると取得できる情報一覧を確認できる。

```sh
$ system_profiler -listDataTypes
vailable Datatypes:
SPParallelATADataType
SPUniversalAccessDataType
SPSecureElementDataType
SPApplicationsDataType
SPAudioDataType
SPBluetoothDataType
SPCameraDataType
...
```
