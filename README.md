# follow-through

让 agent 记住还没收尾的事，定时核实，有新变化才找你，而且每次只带一个现成动作。它交付给你的东西也会先自查，交付后再复查一次，有证据才算闭环。

追踪、巡检、自查三合一，学术和生活场景都能用。

## 安装（让你的 agent 照做）
1. 把仓库下载到它的工作区，比如 `git clone <本仓库地址> followthrough`
2. 把 `templates/` 里的三个文件复制到 `followthrough/` 目录，然后填好 `CONFIG.md`
3. 按平台挂载：
   - Hermes：把 SKILL.md 放进 `~/.hermes/skills/follow-through/`。建一个每天的 cron 并挂上这个 skill；有早报的话，合并进早报，不要另开一个。
   - OpenClaw / Claude Code / 其他：把 `RULES-paste.md` 的内容贴进系统提示或 AGENTS.md，再用它自带的定时任务每天触发一次"执行 follow-through 巡检"。
4. 先试行 3 天：只写日志，不推送。第 4 天它会主动来问你"这条准吗"。

## 文件
- `SKILL.md`：完整规则
- `templates/`：配置、追踪清单、日志的模板
- `RULES-paste.md`：给没有 skill 系统的 agent 用
