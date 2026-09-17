# 00 申报信息（`submission` 第八组）

> 本文件对应第 0 步的**第八组字段**，仅 `delivery_mode = quality_course` 时存在。
> 普通模式的《劝学》示例**没有这一组**——这就是两种模式在输入侧的差别。

---

## 字段表

| 字段 | 值 | 状态 | 说明 |
|---|---|:-:|---|
| `submission.year` | 2026 | `confirmed` | 用户提供 |
| `submission.category` | **学科课程类** | `confirmed` | 本技能只做这一类 |
| `submission.stage` | 高中 | `confirmed` | — |
| `submission.subject` | 语文 | `confirmed` | — |
| `submission.platform` | 国家中小学智慧教育平台 | `confirmed` | — |
| **`submission.official_title`** | `劝学` | **`needs_verification`** | **平台节点原文尚未取到**。此处取教材目录写法，正式提交前须从平台目录页**原文复制**（见 `01-catalog-node.md`） |
| `submission.textbook_edition` | 人民教育出版社 · 2019 年版 · 必修上册 | **`needs_verification`** | 版次依教材版权页推定；**须与学生实际用书核对**（部分学校用不同印次） |

---

## 三处必须说清的地方

**一、这一组不是"顺手多加的一栏"。**

它决定后面全部工作的边界：

```
official_title  →  节点锁 → 教材版本 → 单元 → 任务群 → 水平 → 素养 → 目标
```

如果 `official_title` 取错（例如实际节点是《劝学（节选）》而这里写《劝学》），**后面九步全部要重做**。

**二、状态标记一个都不能省。**

`official_title` 与 `textbook_edition` **两项都标 `needs_verification`，不是 `confirmed`**，因为：

- 平台节点会调整，且名称口径以平台为准；
- 教材版次须与**学生手上的那本书**核对，不是与"统编版"这个笼统说法核对。

这两项在普通模式里最容易被"默认统编版"糊过去；在本模式下**它们直接决定节点能不能交**。

**三、本组填完 ≠ 节点已锁。**

填表只是把输入摆出来；**核验是第 0.5 步的事**，且那一步**不做降级**。见 `01-catalog-node.md`。

---

## 与普通模式《劝学》示例的对照

| | 普通模式示例 | 精品课示例（本目录） |
|---|---|---|
| 第八组 `submission` | **不存在** | **必填 7 个字段** |
| 起点 | 篇目《劝学》 | **平台目录节点** |
| 依据链起头 | 课标 → 任务群 | **官方节点 → 教材 → 单元** → 任务群 |
| 交付 | 四份 Word ＋ 课件 | 四件套 ＋ 微课运行稿 |
| 冻结次数 | 一次 | **两次** |

> **`delivery_mode` 的取值**：本目录全部文件都建立在 `delivery_mode = quality_course` 之上。
> 注意这不是 `lesson_type.mode`（那个是讲读 / 自读 / 活动）——**三者互不相干**。
