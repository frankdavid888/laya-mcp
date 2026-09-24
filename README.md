##Laya MCP 便携安装包##
把开源的非自回归「System 1」决策引擎 Laya 打包成 MCP 服务，一键装进 Codex、Claude Code、Gemini、Grok、OpenCode 等 AI 编码助手，给它们增加一个本地、毫秒级、免解析的类型化决策工具。

##一句话定位##
不用再让大模型「输出 JSON 再解析」——用 Laya 对文本 / JSON 做一次前向传播，直接得到带置信度的分类、打分、是否判断。

##决策原语##
原语	输出	典型用途
choice	最优标签 + 各选项概率 + 置信度	意图分类、部门路由、主题归类
score	有序等级上的期望值	紧急度、挫败感、危害等级
noul	P(true) 校准概率	是否钓鱼 / 垃圾 / 越狱、流失风险


##核心特性##
- 真正傻瓜式：双击 install.bat 全自动完成，全程中文提示。
- 多助手适配：自动检测 8 个 AI 助手及其版本，并注册进能自动配置的助手。
- 版本检测：打印 Python / laya / mcp / torch 以及各助手的版本号。
- 幂等 + 自愈：重复安装不重复写配置；发现损坏的旧虚拟环境会自动重建。

##包内容##
install.bat（双击入口）、install.ps1（安装逻辑）、laya_mcp_server.py（MCP 服务）、register_agents.py（助手检测+注册）、README.md、DESCRIPTION.md、models/（内置模型）。
##支持的助手##
Claude Code、Codex、Gemini CLI、Grok、OpenCode 这五个检测后自动注册；OpenClaw、Hermes、Pi 检测 + 中文提示手动接入。
##使用三步##
1. 把整个文件夹拷到目标电脑（路径不带中文和空格）；
2. 双击 install.bat，等待完成；
3. 重启对应助手，即可调用 laya_health / laya_decide / laya_preset。
##环境要求##
Windows 10/11，装了上述任一助手；一次性联网下载 Python 依赖（约几百 MB），模型离线；无需 GPU。
