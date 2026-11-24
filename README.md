# surge-rules

Surge 远程规则集：自有 Emby 服务器分流清单。

- `emby-proxy.list`：需要走代理的 Emby 服务器，走 `NewFly` 组。
- `emby-direct.list`：可以直连的 Emby 服务器，走 `DIRECT`。

每行一条规则，格式 `DOMAIN-SUFFIX,example.com`。域名由用户逐台筛选后填入，不抄任何第三方的清单。

托管配置引用方式（Surge `[Rule]`）：

```
RULE-SET,https://raw.githubusercontent.com/wocaorencuo/surge-rules/main/emby-proxy.list,☄️ newFly
RULE-SET,https://raw.githubusercontent.com/wocaorencuo/surge-rules/main/emby-direct.list,DIRECT
```
