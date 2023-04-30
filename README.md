# 🚀 shadowrocket-rules

<p align="center">
  <a href="https://github.com/GMOogway/shadowrocket-rules/stargazers">
    <img src="https://img.shields.io/github/stars/GMOogway/shadowrocket-rules?label=Stars&style=social">
  </a>
  <a href="https://github.com/GMOogway/shadowrocket-rules/fork">
    <img src="https://img.shields.io/github/forks/GMOogway/shadowrocket-rules?label=Fork&style=social">
  </a>
</p>

```
    /\_____/\   💖
   / ⭐  ⭐ \
  ( ==  ^  == )   如果觉得有点用
   )         (   请随手给个小星星
  (           )    鼓励一下呗💖
 ( (  )   (  ) )
(__(__)___(__)__)
```

小火箭规则，小火箭配置，shadowrocket规则，shadowrocket rules，最全面的直连（`DIRECT`）、代理（`PROXY`）、屏蔽（`REJECT`）规则，数据最全面，自动构建，每日更新。欢迎 PR，共同完善。
- 最后更新时间：2023-05-01 06:34:18
- DIRECT规则数：65703，update -24
- PROXY 规则数：18974，update +0
- REJECT规则数：59775，update +94

## 使用方法

- 复制 [小火箭极简配置](https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/docs/03.shadowsocks_tiny.conf) 链接，在 `小火箭 -> 配置 -> 远程文件` 中添加，不到20行，直接复制内容新建一个配置也行
- `小火箭 -> 配置 -> 模块`，右上角，添加三个规则（[模块化规则链接](#规则下载)）
- 完成，精准分流，愉快上网
- 想要自动更新规则，请参考 [02.shadowrocket_update_modules.md](https://github.com/GMOogway/shadowrocket-rules/blob/master/docs/02.shadowrocket_update_modules.md)

>高级选手请任意搭配使用。如果使用白名单模式，加载 `sr_direct_list.module` ，后面跟一句 `GEOIP,cn,DIRECT` ，避免一些国内新域名走了代理（详见 [issues #7](https://github.com/GMOogway/shadowrocket-rules/issues/7)），最后 `FINAL,PROXY` 即可；如果使用黑名单模式，加载 `sr_proxy_list.module` ，最后 `FINAL,DIRECT` 即可；在上面的基础上，如果想去广告，加载 `sr_reject_list.module` 即可。

>关于小火箭模块的优先级问题这儿解释一下，第一：模块中的规则优先于配置中的规则，第二：多个模块，上面的模块优先级比下面的要高，在模块中可以自行调整模块的上下。清楚了以上两点，就可以配出你想要的效果了。

>有小伙伴提出问题：你这模块化规则使用以后，我原来有些特殊的规则被覆盖掉，不起作用了。是的，虽然这些模块化规则适应了普遍性的使用需求，但前面也说了，模块的优先级高于配置，就会产生这个问题。理想的解决方案是你自建一个小小的模块，把你的特殊规则写到里面，然后把这个模块移到上面去，这时它就会最优先匹配处理了。

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
>每类规则提供了二个链接，一个需要代理才能访问，一个可以直接访问，请根据实际情况选择，只是jsdelivr会延迟12小时，但对于几万条的规则来说，没什么影响。

## 帮助文档

- [01.shadowrocket_configure.md](https://github.com/GMOogway/shadowrocket-rules/blob/master/docs/01.shadowrocket_configure.md)，比较全面的介绍了shadowrocket小火箭的配置文件
- [02.shadowrocket_update_modules.md](https://github.com/GMOogway/shadowrocket-rules/blob/master/docs/02.shadowrocket_update_modules.md)，介绍了如何手动或自动更新shadowrocket小火箭规则模块
- [03.shadowsocks_tiny.conf](https://raw.githubusercontent.com/GMOogway/shadowrocket-rules/master/docs/03.shadowsocks_tiny.conf)，一个小火箭的极简配置，不到20行，容易修改编辑吧？再配上本项目提供的规则，即可精准分流、愉快上网

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
