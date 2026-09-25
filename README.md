# Shadowrocket 最简配置

国内网站直连，国外网站和 AI 服务走你当前选中的节点。不含广告拦截，也不含节点，节点用你自己的订阅。

## 使用

1. Shadowrocket →「配置」→ 右上角 `+` → 粘贴下面的地址 → 下载：
   ```
   https://raw.githubusercontent.com/Bergpss/shadowrocket-config/main/berg.conf
   ```
   下载失败的话先连上任意节点，把全局路由切到「代理」再下载。
2. 点下载好的 `berg.conf` →「使用配置」。
3. 首页「全局路由」选「配置」。
4. 以后更新：「配置」里点 `berg.conf` →「更新」。

## 规则

| 流量 | 走向 |
|---|---|
| AI 服务（Claude、ChatGPT、Gemini、Grok、Perplexity 等） | 当前选中的节点（用 AI 的话，节点要选美国等支持地区） |
| 国外常用网站（按域名清单） | 当前选中的节点 |
| 国内网站（按域名清单） | 直连 |
| 其他：国内 IP 直连，其余走代理 | — |

DNS 用阿里 `223.5.5.5` 和腾讯 `119.29.29.29` 的普通查询。国内网站按域名清单直连，不依赖 DNS 解析出的 IP，避免国内网站被绕到海外节点。

规则清单来自 [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script) 和 [iab0x00/ProxyRules](https://github.com/iab0x00/ProxyRules)，由它们的作者持续更新。
