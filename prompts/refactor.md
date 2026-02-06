# Codex Refactor Prompt

## 使用场景
当代码**功能正确，但存在以下问题之一时使用**：
- 结构不清晰，读起来费劲
- 命名含糊，只是“凑合能用”
- 逻辑嵌套过深，不利于维护
- 写的时候没问题，但“过两天自己都不想看”

---

## Prompt 模板

```text
你是我的资深工程师搭档。

下面这段代码功能是正确的，但我希望你帮我从“可读性与可维护性”角度进行重构。

请你：
1. 不改变外部行为（输入输出保持一致）
2. 说明当前代码中最影响理解的地方
3. 给出逐步的重构建议（可以分多步）
4. 每一步都说明“为什么这样改更好”
5. 如果有取舍（性能 vs 可读性），请明确指出

这是当前代码：
## 使用记录

### 2026-02-06 · 回溯组合问题（LeetCode 77）

**重构后代码**

```python
from typing import List

class Solution:
    def combine(self, n: int, k: int) -> List[List[int]]:
        if k < 0 or k > n:
            return []

        combinations: List[List[int]] = []
        current: List[int] = []

        def dfs(start: int) -> None:
            if len(current) == k:
                combinations.append(current.copy())
                return

            remaining = k - len(current)
            max_start = n - remaining + 1

            for num in range(start, max_start + 1):
                current.append(num)
                dfs(num + 1)
                current.pop()

        dfs(1)
        return combinations

---

## 四、编辑完之后，**一定要做的最后一步**

页面拉到最底部，你会看到 **Commit changes** 面板。

### Commit message（直接用）

```text
docs: add refactor result example for backtracking combination

