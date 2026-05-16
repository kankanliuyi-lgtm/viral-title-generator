# 🔥 X爆款标题生成器 | Viral Title Generator Skill

> Agent Skill — 基于116条真实X/Twitter爆款标题（阅读量10万-260万+）提炼的12种标题公式，一键生成高点击率标题。
>
> **兼容平台：** Claude.ai · Claude Code · Codex (OpenAI) · OpenClaw · 及所有支持 SKILL.md 标准的 Agent

**作者：** [运营老李搞AI](https://x.com/kankan916033)

---

## 这是什么？

一个 Agent Skill（智能体技能插件），安装后说"帮我想个爆款标题"，它会：

1. **分析你的内容** → 自动识别内容类型和核心卖点
2. **匹配最佳套路** → 从12种爆款公式中推荐2-3种
3. **生成候选标题** → 每种套路3个，共6-9个候选
4. **评分自检** → 5维度打分（好奇心/具体性/情绪感/可搜索性/行动驱动）
5. **给出TOP 3** → 附优化建议和A/B测试方向

也支持**标题优化模式**：丢一个现有标题进去，自动诊断问题 + 改写优化。

---

## 12种标题套路一览

| # | 套路 | 核心公式 | 代表案例 |
|---|------|---------|---------|
| 1 | 数字清单型 | [数字] + [工具] + [利益] | 这10个ChatGPT提示词感觉非法（但不违法） |
| 2 | 震惊情绪型 | [情绪词] + [悬念] + [内容] | 卧槽！这个工具绝了！ |
| 3 | 利益诱惑型 | [低门槛] + [收益数字] + [方法] | 笔记本+WiFi，每天赚500美元 |
| 4 | 争议吐槽型 | [争议观点] + [对象] + [情绪] | gemini现在是美国版豆包 中看不中用 |
| 5 | 故事案例型 | [人物] + [反差结果] + [方法] | 我朋友用ChatGPT减掉了20公斤 |
| 6 | 教程保姆级型 | [降门槛词] + [技能] + [效果] | 全网最细Claude Code零基础教程 |
| 7 | 工具发现型 | [发现感] + [工具名] + [能力] | 在GitHub挖到一个好用的工具 |
| 8 | 趋势认知型 | [类比] + [趋势判断] + [行动] | AI就像19年短视频：最大红利期 |
| 9 | 公式等式型 | A + B + C = 结果 | 美貌 + 性感 + 免费 = 流量密码 |
| 10 | 紧急行动型 | [紧迫感] + [行动] + [利益] | 刷到这套提示词，请立即搬运！ |
| 11 | 对比VS型 | A vs B + [结论] | 中国AI应用 vs 美国工具：对标清单 |
| 12 | 禁忌边界型 | [禁忌暗示] + [工具] + [突破] | ChatGPT有一个隐藏模式 |

---

## 安装方法

### Claude.ai（网页/App）

1. 下载 [viral-title-generator.skill](./viral-title-generator.skill) 文件
2. 打开 [claude.ai](https://claude.ai) → 设置 → Skills
3. 点击添加 → 选择下载的文件 → 完成

### Claude Code（终端）

```bash
# 方法1：全局安装（所有项目可用）
mkdir -p ~/.claude/skills/viral-title-generator
cp viral-title-generator/SKILL.md ~/.claude/skills/viral-title-generator/
cp -r viral-title-generator/references ~/.claude/skills/viral-title-generator/

# 方法2：项目级安装（仅当前项目可用）
mkdir -p .claude/skills/viral-title-generator
cp viral-title-generator/SKILL.md .claude/skills/viral-title-generator/
cp -r viral-title-generator/references .claude/skills/viral-title-generator/
```

安装后在 Claude Code 中输入 `/viral-title-generator` 或直接说"帮我想个爆款标题"即可触发。

### Codex（OpenAI）

```bash
# 方法1：全局安装
mkdir -p ~/.agents/skills/viral-title-generator
cp viral-title-generator/SKILL.md ~/.agents/skills/viral-title-generator/
cp -r viral-title-generator/references ~/.agents/skills/viral-title-generator/

# 方法2：项目级安装
mkdir -p .agents/skills/viral-title-generator
cp viral-title-generator/SKILL.md .agents/skills/viral-title-generator/
cp -r viral-title-generator/references .agents/skills/viral-title-generator/
```

安装后在 Codex 中输入 `$viral-title-generator` 或直接描述需求即可触发。

### OpenClaw

```bash
# 方法1：手动安装
mkdir -p ~/.openclaw/skills/viral-title-generator
cp viral-title-generator/SKILL.md ~/.openclaw/skills/viral-title-generator/
cp -r viral-title-generator/references ~/.openclaw/skills/viral-title-generator/

# 方法2：直接从GitHub安装（在OpenClaw对话中输入）
Install this skill: https://github.com/kankanliuyi-lgtm/viral-title-generator
```

安装后重启 OpenClaw gateway 生效。

### 通用安装（任何支持 SKILL.md 的 Agent）

核心就是把 `viral-title-generator/` 文件夹放到你的 Agent 的 skills 目录下：

```
你的Agent的skills目录/
└── viral-title-generator/
    ├── SKILL.md
    └── references/
        └── title_formulas.md
```

---

## 使用方法

安装后，在任意对话中输入：

**生成新标题：**
```
帮我写一个关于[你的内容主题]的爆款标题
```

**优化已有标题：**
```
帮我优化这个标题："[你的标题]"
```

**指定平台：**
```
帮我写一个发公众号/抖音/视频号的标题，内容是[主题]
```

---

## 效果示例

**输入：**
> 帮我写一个关于Codex评测的标题

**输出（TOP 3）：**

| 排名 | 标题 | 评分 | 套路 |
|------|------|------|------|
| 🥇 | Codex的5个隐藏玩法，第3个感觉不太合法（但真的能用） | 88分 | 数字清单+禁忌边界 |
| 🥈 | 卧槽！Codex做完一个项目只用了10分钟，我之前花了3天 | 86分 | 震惊情绪型 |
| 🥉 | 10个Codex真实用法，第一个就让我卸载了其他AI编程工具 | 85分 | 数字清单型 |

---

## 文件结构

```
viral-title-generator/
├── SKILL.md                          # 核心指令（生成流程+评分+自检）
└── references/
    └── title_formulas.md             # 12种套路详细参考库（含真实案例+阅读量数据）
```

---

## 数据来源

基于X/Twitter平台116条去重爆款帖子分析，覆盖：
- AI工具评测、提示词分享、赚钱变现、自媒体运营等赛道
- 阅读量范围：2万 - 260万+
- 数据采集时间：2025年

---

## 适合谁用

- 🎯 AI自媒体创作者
- 🎯 公众号/视频号/抖音运营
- 🎯 X/Twitter中文博主
- 🎯 需要写标题的任何内容创作者

---

## 平台兼容性

| 平台 | 安装方式 | 触发方式 | 状态 |
|------|---------|---------|------|
| Claude.ai | .skill文件导入 | 自然语言 | ✅ 已验证 |
| Claude Code | ~/.claude/skills/ | `/skill` 或自然语言 | ✅ 兼容 |
| Codex (OpenAI) | ~/.agents/skills/ | `$skill` 或自然语言 | ✅ 兼容 |
| OpenClaw | ~/.openclaw/skills/ | 自然语言 | ✅ 兼容 |
| Cursor | .cursor/skills/ | 自然语言 | ✅ 兼容 |
| Gemini CLI | 同 Claude Code 格式 | 自然语言 | ✅ 兼容 |

> SKILL.md 是 Agent Skills 开放标准格式，所有支持该标准的平台均可使用。

---

## 反馈 & 贡献

- 有好的爆款标题案例？欢迎提 Issue 补充
- 发现套路分类不准？欢迎提 PR 优化
- 使用中有问题？欢迎在 X 上 @运营老李搞AI

---

## License

MIT License — 随便用，注明出处就行。

---

**如果觉得有用，给个 ⭐ Star 支持一下！**
