# outcome-first

以结果为导向的 AI 协作技能：简单任务直接做；复杂任务理解实际目的，按需改进方法，并交付有验证依据的结果。

## 适用场景

- 改进反复发生、耗时较多的工作流程。
- 检查已有判断，区分事实、猜测与推断。
- 为任务引入真正有用的专业方法。
- 用小实验尝试更高目标，计入检查和纠错成本。

普通问答、简单改写和目的明确的小任务不会被要求走完整流程。用户不需要填写提示词模板。

## 安装与使用

将本仓库作为 `outcome-first` 文件夹放入 Codex 的技能目录。默认目录为 `~/.codex/skills`；使用自定义 `CODEX_HOME` 时，放入其 `skills` 子目录。

默认配置下可执行以下命令（目标文件夹需尚不存在）：

```sh
git clone https://github.com/you615074-png/outcome-first.git ~/.codex/skills/outcome-first
```

在支持技能加载的会话中使用：

```text
用 $outcome-first 帮我推进这件事：……
```

技能允许自动选择，但不会给自己增加操作权限，也不要求多代理协作。

## 文件

- [SKILL.md](SKILL.md)：完整协作方法与适用边界。
- [agents/openai.yaml](agents/openai.yaml)：显示名称、默认提示与调用设置。

## 思路来源

受到 Felix Rieseberg 的 [How to be more ambitious: A tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/) 启发，并整理为强调用途、专业方法、可验证实验和轻量协作的技能。本项目是独立整理的实践版本，不代表原作者或 Anthropic 官方。

## 验证范围

技能已通过 skill-creator 的格式校验；这不等于已经证明它能在所有任务中改善结果。应根据实际使用效果继续调整。
