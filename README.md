# MiniMax H3 人物表演导演

把人物动机、情绪路径、细微表情、对白和动作时间预算，转换为 MiniMax H3 的官方提示词结构。独立于 Seedance 版本，可单独安装；属于自建适配版，不是 MiniMax 官方 Skill。

官方基础能力来自 [h3-prompt-writing](https://github.com/MiniMax-AI/MiniMax-H3/tree/main/skills/h3-prompt-writing)。我们在它的模式与格式规则之上加入人物表演设计：先处理反应因果、可见细节、控制意图、动作连续性和时长，再输出 H3 所需正文。

| 内容 | Seedance 人物表演版本 | 本 H3 适配版 |
| --- | --- | --- |
| 人物设计 | 动机、情绪、表演、时间预算 | 保留并加入本次细微表情优化 |
| 默认正文 | 中文场景与分秒时间段 | 英文结构字段，中文对白保留原文 |
| 输入组织 | 按用户平台与素材适配 | 明确 T2VA、I2VA、FL2VA、L2VA、Ref2VA |
| 镜头时间 | 中文段落节奏 | `[Shot 1]` 与后续真实切点；表演节拍不强制切镜 |
| 参考管理 | 身份、场景、动作与接续分工 | 增加官方标签、保留关系与发声编号 |
| 长片 | 先设计总片长再核实平台 | 按官方 4–15 秒单段写作范围拆段，并核对实际平台 |

## 使用

将完整的 `minimax-h3-performance-director` 目录放入 `~/.codex/skills/`，保留 `references/` 与 `agents/`。已存在时先检查现有修改。无需安装官方 Skill、下载模型或配置 API；本包只负责设计与写作。

也可通过 Git 安装到尚不存在的技能目录：

```bash
git clone https://github.com/geslie1/minimax-h3-performance-director.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/minimax-h3-performance-director"
```

```text
使用 $minimax-h3-performance-director。
H3 文生音视频，8 秒固定近景。成年负责人收到项目取消的消息，
仍平稳回答：“知道了，先把文件收好。”
全程成功控制表情，不哭、不颤抖；只给最终提示词。
```

```text
使用 $minimax-h3-performance-director。
人物图只参考身份，视频只参考动作，音频只参考音色。
12 秒，保留我的中文台词和结尾，先检查素材分工，
再按 Ref2VA 格式输出，不带入参考视频的原演员和原台词。
```

默认给中文导演说明、一个可复制的英文结构正文和简短文字校核。明确要求只给提示词或只改局部时按要求交付。

## 文件

- [SKILL.md](SKILL.md)：模式选择、人物设计、H3 编译与交付检查。
- [基础模式](references/h3-base-format.md) 与 [全参考模式](references/h3-reference-format.md)：H3 的字段、对齐、对白与引用规则。
- [表演细节](references/performance-library.md)、[自然度修复](references/natural-performance.md)、[时间预算](references/timing-and-continuity.md)、[复杂表演](references/complex-performance.md)：按需使用的导演方法。
- [H3 示例](references/examples.md)：原创基础与全参考正文。
- [来源与适配说明](references/sources.md)：官方链接、读取版本与适配取舍。

本版基于 2026-10-10 核对的官方写作规范。已通过 Skill 结构、相对链接、示例字段／标签检查及独立协议审查，并完成六条文字试用：T2VA、I2VA、FL2VA、L2VA 各一条，以及 Ref2VA 音色参考、视频编辑与整轨复制各一条。检查覆盖原话保留、发声编号、关键帧状态、动作时间和指定结尾；尚未进行 H3 实际生成测试。

## License

[MIT](LICENSE) © 2026 geslie1。许可覆盖本包原创内容及自有表演方法；引用的官方资料仍由其权利人持有，未随包复制全文。
