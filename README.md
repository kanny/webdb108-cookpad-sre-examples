# webdb108-https-example
このレポジトリは、2018年12月22日発売の[WEB+DB PRESS Vol.108](http://gihyo.jp/magazine/wdpress/archive/2018/vol108)に掲載されている 「大規模インフラ解体新書」連載のサンプル設定です。

# サンプルの利用方法
レポジトリに含まれるサンプルは [osquery](https://osquery.io/) および [td-agent (Fluentd)](https://www.fluentd.org/download) で利用可能なものです。
誌面にて紹介している環境やインストール方法に沿う場合、以下のファイルパスに配置することで動作することを確認しています。

osquery.conf: `/etc/osquery/osquery.conf`
td-agent.conf: `/etc/td-agent/td-agent.conf`

## コメントの置き換え
設定において #{ ... } と表記されている箇所はコメントになります。
記号部も含めた全てを、コメント内に表記されている形に置き換えてください。

例えば、
```
  port #{GraylogのGELF Inputで設定したポート}
```

は、置き換えると
```
  port 12201
```

となります (12201 番ポートを利用する場合)。