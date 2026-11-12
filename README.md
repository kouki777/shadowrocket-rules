# Shadowrocket 分流规则

`shadowrocket.conf`：B站、拼多多、阿里巴巴（1688/淘宝/天猫/支付宝/阿里云）、代发助手王走代理，其他全部直连。

## 使用方法

1. 在 iPhone 上下载 `shadowrocket.conf`，用「共享 → Shadowrocket」打开，或在 Shadowrocket「配置」页导入。
2. 在「配置」里点这个文件 →「使用配置」。
3. 首页「全局路由」选 **配置**，节点选中 **香港节点**。

规则里的 `PROXY` 指的就是首页当前选中的节点。

## 排查

如果代发助手王仍然卡：Shadowrocket → 数据 / 日志，看看它有哪些域名走了 DIRECT，把域名补进 `[Rule]`；
或者把文件末尾 `# GEOIP,CN,PROXY` 的注释去掉（所有大陆 IP 都会走代理）。
