# ArDNSPod
基于DNSPod用户API实现的纯Shell动态域名客户端，可以当做 keepalived 来使用。

# Usage

1. 复制`dns.conf.example`到同一目录下的`dns.conf`，填充 api 的访问密钥。
1. 复制`domain.list.example`到同一目录下的`domain.list`，填写需要 ddns 的域名。

执行时直接运行`ddnspod.sh`，默认无限 check domain.list 中的域名，并自动选择可用节点。

配置文件格式：
```
# 按`TokenID,Token`格式填写
arToken="12345,7676f344eaeaea9074c123451234512d"

# 每行一个域名
test.org www
```

# 最近更新

2018年03月24日 (by 血衫非弧)
- 自动选择可用节点，替换失效节点。
- 增加节点存活验证，不断 check 域名的可用性。

2015/2/24
- 增加token鉴权方式 (by wbchn)

2015/7/7
- 使用D+服务获取域名解析

2016/2/25
- 增加配置文件，分离脚本与配置，适配内网。
- 加入Mac支持
- sed脚本POSIX化，可跨平台

2016/3/23
- 进一步POSIX化，支持Mac和大部分Linux发行版
- 更改配置文件格式

# Credit

Original: anrip

This version maintained by 血衫非弧
