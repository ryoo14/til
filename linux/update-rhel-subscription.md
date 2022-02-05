# 期限切れしたRed Hat Developer Subscription for Individualsを更新する

RHELなサーバでセキュリティアドバイザリーが出ていたので更新しようとしたらできなかった。

[サブスクリプションのページ](https://access.redhat.com/management/subscriptions)で確認すると、CentOSの死亡と同時に登録していたRed Hat Developer Subscription for Individualsが期限切れしていた。1年で自動更新してくれない模様。

[Red Hat Developer](https://developers.redhat.com/login)にアクセスすると幾つか同意を求められるので、同意すると更新完了らしい。  
期限切れしたサブスクリプションの横に更新ボタンがあったので、それを押してからでないといけないかもしれない。

しばらく待つとアクティブなサブスクリプションとしてRed Hat Developer Subscription for Individualsが追加される。が、そこからしばらく16あるはずのエンタイトルメントが0のまま変わらないので、焦らない。

サーバ側ではコマンドで再登録が必要。

```
# subscription-manager register
usernameとpasswordが求められるので入力
# subscription-manager list --available
表示されるまでにしばらく時間がかかる
# subscription-manager attach --auto
```

`remove`や`unregister`は必要なかったけど、実行している人もいるので場合によるかもしれない。