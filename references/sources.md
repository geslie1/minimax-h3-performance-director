# 来源与适配说明

核验日期：2026-10-10。协议依据来自 MiniMax 官方 GitHub 仓库；本 Skill 是人物表演方法的独立适配，不代表官方背书，也未调用 H3 生成验证。

| 来源 | 本版采用内容 | 已读取的 Git blob SHA |
| --- | --- | --- |
| [官方 h3-prompt-writing](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/SKILL.md) | 模式选择、英文改写、原语言内容保留、4–15 秒写作范围 | `b6d9b2839384a588763a9c24315225dd8ce19d56` |
| [基础模式指南](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/references/base-en.txt) | 三字段、首尾帧对齐、镜头与对白语法、声音分层 | `40cf586a634d677d6b7107b367cf0ec9621be728` |
| [全参考指南](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/references/ref-en.txt) | 六字段、引用标签、保留标记、音色与音轨复用、全局发声编号 | `7ae1b2d07d743fd2392258a96449be9e9e322d35` |
| [MiniMax 官方 H3 入口](https://design.minimax.io/h3) | 官方 Skill 入口及模型／服务端工作流的区分 | 网页，未固定版本 |

表演方法源自我们维护的 [Seedance 人物表演 Skill](https://github.com/geslie1/seedance-2-5-performance-director)，并包含此次依据用户提供的 `seedance-prompt-master` 整理的细微表情修订。随包附带的是我们编写的表演参考、协议摘要和原创示例，没有打包官方指南全文、模型、演示媒体或用户提供的原始资料。

## 适配决策

- 保留动机、刺激接收、表情过程、观众可读性、物体连续性和时间预算；为 H3 单独实现输出层。
- 官方推荐英文结构正文，沟通与导演解释继续使用中文。用户已锁定的中文对白和画面字保留原文。
- 基础指南要求用户台词原样保留；全参考指南另有参考音频转录的标点整理规则。本版区分已定台词与待转录音频，用户逐字要求优先，听不清的片段不猜。
- 完整 Ref2VA 通常按官方建议的 350–500 个英文词写足画面、动作、声音和引用关系；用户要求短稿或局部修改时尊重范围，不为凑词扩剧情。格式符合不等于模型逐帧执行。
- 平台提交参数、素材上限、价格与单次生成能力不由写作模板推导。需要实际执行时再核对相应平台当前文档。

## 维护

官方格式变化时，优先核对以上三份文件的字段、标签、对齐句、对白和音轨规则；只更新受影响的适配参考与示例，再跑基础模式及全参考模式的文字试用。表演参考与 Seedance 版本共享创作方法，但本包不依赖另一个 Skill 的安装路径。
