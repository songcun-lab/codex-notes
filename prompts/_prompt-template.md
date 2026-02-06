# Codex Prompt 通用模板（Template）

本文件定义 **所有 Codex Prompt 的通用结构与使用原则**。  
具体场景（debug / refactor / learn）请使用对应文件。

---

## 一、使用目标

- 让 Codex 以「资深工程师搭档」的身份参与思考
- 关注 **问题定位、思路澄清、决策权衡**
- 避免一次性重写全部代码

---

## 二、通用 Prompt 结构

```text
你是我的资深工程师搭档。

这是当前的背景与问题描述：
[在这里粘贴代码 / 报错 / 场景说明]

请你：
1. 先从整体上判断问题或任务的类型
2. 明确关键约束与隐含假设
3. 给出分步骤的分析思路
4. 提供可执行但不过度的建议
5. 如有多种方案，请说明取舍理由

---

## 五、那你现在写的那些「分类说明 / 示例」去哪了？

👉 **全部应该挪到 `prompts/README.md`**

`prompts/README.md` 的职责是：

- 告诉你：
  - 什么时候用 debug
  - 什么时候用 refactor
  - 什么时候用 learn
- 像一个「使用说明书」

---

## 六、你现在该怎么提交（给你一个明确动作）

### 1️⃣ 整理并保存 `_template.md`
### 2️⃣ Commit message 用这一句（直接抄）

```text
docs: refactor prompt template into a single-purpose base template
