# muse-loon-rules

Meta Muse AI 的 Loon 分流规则订阅。

## 订阅方式

在 Loon「配置」→「规则」中添加远程规则集，URL 任选其一：

- GitHub Raw：https://raw.githubusercontent.com/juner922/muse-loon-rules/main/MuseAI.list
- jsDelivr CDN（国内访问更快）：https://cdn.jsdelivr.net/gh/juner922/muse-loon-rules@main/MuseAI.list

将规则指向你的美国节点策略组。

## 规则说明

- `MuseAI.list`：Muse App 核心域名（`muse.ai` / `metaaivm.com` / `meta.com` 等）+ Meta 账号与社交基础设施（Facebook / Instagram / WhatsApp / fbcdn 等）
- 域名来源：Meta Muse 客户端二进制逆向分析（[mahdi-salmanzade/meta-muse-teardown](https://github.com/mahdi-salmanzade/meta-muse-teardown)），经 GitHub 规则库与 NodeSeek / Linux.do / V2EX 社区实测交叉核实
- 建议搭配上游 [VPSDance/ai-proxy-rules](https://github.com/VPSDance/ai-proxy-rules) 的 `meta-ai.list`（覆盖 `meta.ai` 后缀与 Llama 相关域名）一起使用

## 注意事项

Muse 有地区限制：即使域名全部走代理，若出口 IP 不是美区原生/家宽 IP，仍会提示"尚未在你的国家或地区开放"。请使用美区家宽节点。
