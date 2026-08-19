# AGENTS.md

## Project overview

Hugo 静态站点源码，主题使用嵌套 Git 仓库。

## Technology stack

- 已确认技术：文档/脚本（按文件类型确认）。
- 运行时和依赖版本以仓库配置、锁文件及 README 为准，不凭经验升级。

## Repository structure

- 主要目录：`.github/`、`archetypes/`、`assets/`、`content/`、`public/`、`resources/`、`static/`、`themes/`。
- 关键根文件：`config.toml`。
- 进入子目录时检查更近一级的规则和嵌套 Git 根；生成目录不是源码。

## Setup and dependencies

根目录没有完整安装说明；修改前检查入口、配置和相关子项目文档。
不得复制真实凭据、私有地址或本机认证配置。

## Common commands

未从根配置确认统一命令；不要编造构建或测试步骤。

## Development workflow

1. 阅读规则、README、入口和相关配置。
2. 先运行 `git status --short`，保留现有修改。
3. 只做任务相关的小范围修改，不顺带升级依赖或重写旧实现。
4. 执行最相关的验证并报告结果或验证缺口。

## Testing and validation

- 文档改动核对链接、路径、命令和示例。
- 源码改动运行上方已确认的最小相关命令。
- 浏览器扩展需开发者模式重新加载，并检查 manifest、后台脚本和目标页面行为。
- 无自动测试时记录可重复的人工步骤和预期结果。

## Architecture and conventions

保持现有目录、命名、锁文件与协议边界。第三方/历史镜像优先保持上游兼容，不做无关现代化重构。

## Integration and external systems

外部服务、浏览器权限、文件路径和端点以代码及示例配置为准，只记录非敏感角色。

## Important constraints

- 不读取、输出或提交密码、Token、Cookie、私钥和真实环境配置。
- 不修改生成物/二进制，除非任务明确要求且来源可复现。
- 不确定的环境或业务信息标记：`TODO: Verify this with the project owner.`

## Git and change safety

禁止 `git reset --hard`、`git clean -fd`、强推和覆盖用户修改。Commit、push、部署、外部调用必须有明确授权。

## Known issues and troubleshooting

只记录能由代码、配置或文档确认的问题；排错材料需脱敏，并写明输入、环境与验证方法。

## Agent checklist

- [ ] 已读规则、README、入口和相关配置
- [ ] 已检查 Git 与嵌套仓库状态
- [ ] 命令、路径均有仓库依据
- [ ] 已验证改动或说明缺口
- [ ] 高影响操作已取得授权

## Commit 与 Push 持续授权

- 用户已持续授权：完成本项目的修改并通过相关验证后，及时提交并推送当前分支，无需逐次询问。
- 提交前检查 `git status --short` 和相关 diff；只暂存、提交当前任务产生的文件，不得夹带、覆盖或还原用户已有改动。
- 遵守本文件中更严格的分支、贡献与验证规则。若项目不是 Git 仓库、没有可用远端、处于 detached HEAD、验证失败、当前分支不允许推送或推送失败，应停止对应 Git 操作并向用户说明。
- 本授权不包括强制推送、改写历史、删除分支、部署、生产环境变更或其他外部调用；这些操作仍须另行获得明确授权。
