# domain-rules

`domain-rules` 是一个用于管理和应用域名规则的配置库。该库支持使用 `DOMAIN` 和 `DOMAIN-SUFFIX` 等前缀来定义域名规则，从而灵活地处理各种域名匹配和过滤需求。可以用于代理规则、访问控制列表 (ACL)、网络管理等场景。

## 特性

- 支持多种前缀格式，如 `DOMAIN-SUFFIX` 和 `DOMAIN`等。
- 简洁的规则定义，便于管理和扩展。
- 适用于网络过滤、代理设置、域名解析优化等场景。

## 使用方法

### 规则格式

`domain-rules` 库中的规则主要由以下两种格式组成：

1. **DOMAIN-SUFFIX**: 匹配域名的后缀。  
   例如，`DOMAIN-SUFFIX,google.com` 将匹配所有以 `google.com` 结尾的域名，如 `www.google.com` 和 `mail.google.com`。

2. **DOMAIN**: 精确匹配指定的域名。  
   例如，`DOMAIN,www.google.com` 只会匹配 `www.google.com`，不会匹配 `mail.google.com`。

### 示例规则

以下是一些示例规则：

```bash
DOMAIN-SUFFIX,google.com
DOMAIN-SUFFIX,example.org
DOMAIN,www.example.com
DOMAIN-SUFFIX,cdn.example.net
DOMAIN,www2.example.com
```

### 应用场景

`domain-rules` 可以应用于多个场景：

- **代理规则**: 配置某些域名通过代理服务器访问，而其他域名则直接访问。
- **网络安全**: 屏蔽特定域名或子域名，增强网络安全性。
- **访问控制**: 基于域名的访问控制策略，允许或拒绝访问指定的域名。
- **DNS 优化**: 针对特定域名提供自定义的 DNS 解析规则，优化网络性能。

## 许可证

此项目基于 [MIT License](LICENSE) 开源。
