# 免费节点收集与使用指南

本文收集整理可免费使用的代理节点，定期更新。注意：免费节点速度和不稳定性较差，建议有条件者购买付费服务。

## 免费节点来源

### 1. GitHub 免费节点项目

GitHub 上有多个维护免费节点列表的项目。

### 2. 机场公开试用

部分机场提供每日免费流量，登录后台领取后导出订阅。

### 3. 自建节点

最稳定的方式是用 VPS 自建：

```bash
# V2Ray 一键脚本
bash <(curl -s https://raw.githubusercontent.com/v2fly/fhs-install-v2ray/master/install-release.sh)
```

## 免费节点使用风险

安全警告：
- 陌生人的节点可能记录流量日志
- 可能存在中间人攻击风险
- 速度和稳定性无法保证
- 可能突然失效

建议：仅用于测试，基本需求后尽快换用自建或可靠付费服务。

## 节点质量判断

| 指标 | 优质节点 | 劣质节点 |
|------|---------|---------|
| 延迟 | < 200ms | > 500ms |
| 速度 | > 10Mbps | < 2Mbps |
| 稳定性 | 24h不掉线 | 经常断开 |

---

推荐工具：

- [Clash for Windows](https://clashforwindows.site/) - 最好用的 Clash 客户端
- [ClashMI](https://clashmi.site/) - 轻量级选择
- [FlClash](https://flclash.us/) - 现代代理工具
