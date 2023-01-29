# 🚀 shadowrocket-rules

<p align="center">
  <a href="https://github.com/GMOogway/shadowrocket-rules/stargazers">
    <img src="https://img.shields.io/github/stars/GMOogway/shadowrocket-rules?label=Stars&style=social">
  </a>
  <a href="https://github.com/GMOogway/shadowrocket-rules/fork">
    <img src="https://img.shields.io/github/forks/GMOogway/shadowrocket-rules?label=Fork&style=social">
  </a>

```
    /\_____/\   💖
   / ⭐  ⭐ \
  ( ==  ^  == )   如果觉得有点用
   )         (   请随手给个小星星
  (           )    鼓励一下呗💖
 ( (  )   (  ) )
(__(__)___(__)__)
```

小火箭规则，小火箭配置，shadowrocket规则，shadowrocket rules，最全面的直连（`DIRECT`）、代理（`PROXY`）、屏蔽（`REJECT`）规则。欢迎 PR，共同完善。
- 最后更新时间：2023-01-30 06:34:30
- DIRECT规则数：66078，update +0
- PROXY 规则数：35086，update +0
- REJECT规则数：56091，update +19



## 帮助文档

- [01.shadowrocket_configure.md](https://github.com/GMOogway/shadowrocket-rules/blob/master/docs/01.shadowrocket_configure.md)，比较全面的介绍了shadowrocket小火箭的配置文件
- [02.shadowrocket_update_modules.md](https://github.com/GMOogway/shadowrocket-rules/blob/master/docs/02.shadowrocket_update_modules.md)，介绍了如何手动或自动更新shadowrocket小火箭规则模块

## 数据来源

- https://github.com/felixonmars/dnsmasq-china-list
- https://github.com/v2fly/domain-list-community
- https://github.com/gfwlist/gfwlist
- https://github.com/Loyalsoldier/cn-blocked-domain
- https://easylist-downloads.adblockplus.org/easylistchina+easylist.txt
- https://kb.adguard.com/en/general/adguard-ad-filters#dns-filter
- https://pgl.yoyo.org/adservers
- https://someonewhocares.org/hosts
- https://github.com/crazy-max/WindowsSpyBlocker/tree/master/data/hosts

## 规则特点

- 数据全面，直连（`DIRECT`）列表6万条+、代理（`PROXY`）列表3万条+、屏蔽（`REJECT`）列表5万条+；
- 代理列表加入`telegram`、`gv`、`gmail`、`whatsapp`地址段；
- 使用方便，采用小火箭模块形式，能让自己的配置变得非常简洁，使用方便，随时可以进行切换，白名单、黑名单模式都可以适用，还可以自己决定是否要屏蔽广告网站；
- 每天自动构建，确保最新。

## 规则下载

- **直链（DIRECT）规则**：
  - [https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/sr_direct_list.module](https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/sr_direct_list.module)
  - [https://cdn.jsdelivr.net/gh/GMOogway/shadowrocket-rules@master/sr_direct_list.module](https://cdn.jsdelivr.net/gh/GMOogway/shadowrocket-rules@master/sr_direct_list.module)
- **代理（PROXY）规则**：
  - [https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/sr_proxy_list.module](https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/sr_proxy_list.module)
  - [https://cdn.jsdelivr.net/gh/GMOogway/shadowrocket-rules@master/sr_proxy_list.module](https://cdn.jsdelivr.net/gh/GMOogway/shadowrocket-rules@master/sr_proxy_list.module)
- **屏蔽（REJECT）规则**：
  - [https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/sr_reject_list.module](https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/sr_reject_list.module)
  - [https://cdn.jsdelivr.net/gh/GMOogway/shadowrocket-rules@master/sr_reject_list.module](https://cdn.jsdelivr.net/gh/GMOogway/shadowrocket-rules@master/sr_reject_list.module)

## 使用方法

打开小火箭 -> 配置 -> 模块，右上角添加。请注意，此规则列表为`[Rule]`部分，会自动整合至你当前配置中。
- 如果使用白名单模式，加载 `sr_direct_list.module` ，最后 `FINAL,PROXY` 即可；
- 如果使用黑名单模式，加载 `sr_proxy_list.module` ，最后 `FINAL,DIRECT` 即可；
- 在上面的基础上，如果想去广告，加载 `sr_reject_list.module` 即可。

## 常见问题

- **为什么以小火箭模块的形式提供？**

> 相对于提供完整配置，提供模块纯规则的形式更加灵活，因为基本设置和证书、解密每个人不一样，而且模块形式会使得你的配置非常的简洁，容易编辑修改。

- **模块中的规则与我自己的规则哪个优先级高？**

> 模块中规则优先级高。作者也说了，模块是一组覆盖当前配置的设置，可以使用模块来改变部分设置。

- **上千行的代理规则，会对上网速度产生影响吗？**

> 不会的，50000 行的规则和 50 行的规则在 ShadowRocket 中均为同一量级的时间复杂度 O(1)。

- **你提供了这么多规则，如何选择适合我的？**

> 最常用的规则是黑名单和白名单。区别在于对待 `未知网站` 的不同处理方式，黑名单默认直连，而白名单则默认使用代理。如果你选择恐惧症爆发，那就两个都下载好了，黑白名单切换使用，天下无忧。

- **你提供了这么多规则，却没有我想要的 o(>.<)o**

> 有任何建议或疑问，[请联系我](#问题反馈)。

- **广告过滤不完全？**

> 该规则并不保证 100% 过滤所有的广告，尤其是视频广告，与网页广告不同的是，优酷等 App 每次升级都有可能更换一次广告策略，因此难以保证其广告屏蔽的实时有效性。而油管广告则不能通过简单的 url 匹配实现完全去广告。

## 问题反馈

任何问题欢迎在 [Issues](https://github.com/GMOogway/shadowrocket-rules/issues) 中反馈。

你的反馈会让此规则变得更加完美。

## 贡献代码？

通常的情况下，对 [factory 目录](https://github.com/GMOogway/shadowrocket-rules/tree/master/factory) 下的 6 个 .txt 文件做对应修改即可，可以对三个规则作添加或删除。
