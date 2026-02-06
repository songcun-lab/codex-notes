# Codex Prompts 使用说明

本目录用于存放 **我在不同场景下与 Codex 协作的 Prompt 资产**。

目标不是“写出最聪明的 Prompt”，  
而是 **在不同任务中，稳定地获得高质量思考与建议**。

---

## 文件说明

### `_prompt-template.md`
- 所有 Prompt 的 **通用骨架**
- 定义 Codex 的角色、思考方式和输出要求
- 一般不频繁修改，作为“基类”存在

---

### `debug.md`
**使用场景：**
- 代码报错
- 行为异常
- “我知道不对，但说不清哪里不对”

**核心目标：**
- 帮我定位问题层级
- 给出最小修改建议
- 理解「为什么会出问题」

---

### `refactor.md`
**使用场景：**
- 代码能跑，但不满意
- 结构复杂、可读性差
- 想优化但不想推翻重写

**核心目标：**
- 识别坏味道
- 给出渐进式重构方案
- 明确重构的取舍与风险

---

## 使用原则

- 一个 Prompt 文件 = 一个明确场景
- 一个问题只用一个 Prompt
- Prompt 本身也是长期资产，可持续演化

---

## 推荐使用流程

1. 先判断当前任务属于哪一类（debug / refactor / learn）
2. 打开对应 Prompt 文件
3. 基于 `_prompt-template.md` 的结构填写具体上下文
4. 使用 Codex 后，将关键收获回写到 Prompt 或 logs 中
docs: add usage guide for Codex prompt collection
