# sing-box 一键安装与管理脚本，个人自用版本

基于 233boy/sing-box 脚本修改，支持 VMess / VLESS / Trojan / Hysteria2 / TUIC / Shadowsocks / AnyTLS / REALITY 等协议，自动配置 TLS（Caddy）、systemd / OpenRC 服务。

## 安装

```bash
bash <(wget -qO- -o- https://raw.githubusercontent.com/huohuczq/mysb/main/install.sh)
```

或从本仓库源码安装：

```bash
git clone https://github.com/huohuczq/mysb
cd mysb && bash install.sh -l
```

## 使用

安装后运行 `sb` 或 `sing-box` 进入管理菜单。

常用命令：

```bash
sb              # 管理菜单
sb add          # 添加节点配置
sb info         # 查看节点信息/分享链接
sb help         # 完整命令帮助
sb update sh    # 更新脚本
sb update core  # 更新 sing-box 内核
```

## 说明

- 默认生成 VLESS-REALITY（Vision 流控）节点
- 支持 Ubuntu / Debian / CentOS / SUSE / Alpine（amd64 / arm64）
- 修改脚本后推送，CI 会自动打包发布 `code.tar.gz`，供 `sb update sh` 自更新使用
