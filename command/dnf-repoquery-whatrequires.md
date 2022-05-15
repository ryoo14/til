# dnfで指定したパッケージに依存しているパッケージを検索する

```bash
$ dnf repoquery --whatrequires dnf
Last metadata expiration check: 0:12:00 ago on Sun 15 May 2022 01:27:36 PM JST.
auter-0:1.0.0-6.fc35.noarch
calamares-0:3.2.41.1-1.fc35.x86_64
copr-builder-0:0.52-2.fc35.x86_64
copr-builder-0:0.56-1.fc35.x86_64
cpanspec-0:1.78-41.fc35.noarch
dnf-automatic-0:4.12.0-1.fc35.noarch
dnf-automatic-0:4.9.0-1.fc35.noarch
dnf-plugin-diff-0:1.1-9.fc35.noarch
dnf-utils-0:4.0.23-1.fc35.noarch
dnf-utils-0:4.1.0-1.fc35.noarch
dnfdragora-0:2.1.0-5.fc35.noarch
...
```

既にインストール済みのパッケージだけで絞る場合は`--installed`オプション

```bash
dnf repoquery --whatrequires dnf --installed
dnfdragora-0:2.1.0-5.fc35.noarch
system-config-language-0:3.5.0-7.fc35.noarch
yum-0:4.12.0-1.fc35.noarch
```
