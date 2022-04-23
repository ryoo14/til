# 非Rails環境で`rake db:migrate`する時に環境変数でadapterを変える

勘違いしていた話。

下のようなファイル構成の時。

`config/database.yaml`

``` yaml
test:
  adapter: sqlite3
  database: db/test.sqlite3
  timeout: 5000

development:
  adapter: postgresql
  pool: 5
  timeout: 5000
```

`Rakefile`

``` ruby
require 'sinatra/activerecord'
require 'sinatra/activerecord/rake'
require 'yaml'

config = YAML.load_file('./config/database.yml')
ActiveRecord::Base.establish_connection(config[ENV['HOGE_ENV']])
```

ローカルでテストする際に`HOGE_ENV='test' bundle exec rake db:migrate`ってやってるのにpostgresqlの諸々がないよって怒られる。

どうするかというと、`RACK_ENV='test' HOGE_ENV='test' bundle exec rake db:migrate`とすればよい。

つまり、自前の変数を用意しなくても`RACK_ENV`を使えばいいだけだったという話でした。
