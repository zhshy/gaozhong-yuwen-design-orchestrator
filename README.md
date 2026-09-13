# 高中语文教学设计总控

> 把五个语文教学技能串成一条固定工作流的编排层。从定依据到读文本、定教学点、落课堂、做检测，六步走完一节课。

## 这个技能做什么

**不装新知识，只做编排与分流。**

接到一个完整备课任务后，判断该调哪几个技能、按什么顺序调、每个技能交出什么、交接时检查什么。

## 编排的五个技能

| 技能 | 解决什么问题 |
|---|---|
| `gaozhong-yuwen-kebiao` | 依据在哪里、要求到什么水平 |
| `sunshaozhen-text-analysis` | 文本怎么读深 |
| `wang-rongsheng-reading-design` | 教什么、按什么顺序教 |
| `xiaopeidong-qianqian-teaching` | 课堂上怎么落地 |
| `chinese-lesson-design` | 交付格式长什么样 |

## 六步流程

```
0 确认输入（篇目/课型/课时/学情）
1 课标     → 任务群 + 水平 + 素养落点      定边界
2 孙绍振   → 文本关键点 + 核心提问          读深
3 王荣生   → 教学点 + 三个台阶              定教什么
4 肖培东   → 教学出口 + 主问题 + 朗读       落课堂
5 语文设计 → 九项成稿                       交出去
6 检测     → 评价任务 + 评分量规            闭环
```

## 四个卡口

- **卡口一（第 2 步出口）**：每个分析点落到具体语句了吗？说不出是哪几个字、哪个动作，就是没做完
- **卡口二（第 3 步出口）**：教学点 = 文本关键点 × 学生疑难处，重合了吗？
- **卡口三（第 4 步出口）**：每个活动都能指回具体的字词句吗？指不回去，就是飘了
- **卡口四（第 6 步出口）**：每个检测任务都能指回一个教学点吗？题型与体裁匹配吗？

## 分流原则

**用户要的是"一节课"，走全流程；用户要的是"一节课里的某个零件"，直接给那个技能。**

不是所有请求都该走完整流程——上来就跑六步是形式主义。

## 三处已知冲突及处理

| 冲突 | 处理 |
|---|---|
| 任务群 vs 单篇 | 课标按任务群组织，王荣生对单元/群文/项目化审慎。遇单元整体设计时两条路并呈，由用户定 |
| "教得深" vs "教得浅" | 不矛盾：深是备课的深度，浅是上课的姿态 |
| 格式技能与王荣生重叠 | 内容决策层从王荣生，格式配套层从语文设计；冲突时以王荣生为准 |

| 文件 | 内容 |
|---|---|
| `SKILL.md` | 分流表、六步流程、冲突裁决、十条红线、呈现方式 |
| `references/flow-checklist.md` | 一页速查：技能选择树、流程交接物、四个卡口、分层检查清单 |

## 依赖

本技能需要配合上述五个技能使用，它们在 GitHub 上的地址：

- <https://github.com/zhshy/gaozhong-yuwen-kebiao>
- <https://github.com/zhshy/sunshaozhen-text-analysis>
- <https://github.com/zhshy/wang-rongsheng-reading-design>
- <https://github.com/zhshy/xiaopeidong-qianqian-teaching>
- <https://github.com/zhshy/chinese-lesson-design>

## 安装

```bash
git clone https://github.com/zhshy/gaozhong-yuwen-design-orchestrator.git
```

将技能目录放入 WorkBuddy 的用户级技能目录：

- **Windows**：`C:\Users\<用户名>\.workbuddy\skills\`
- **macOS / Linux**：`~/.workbuddy/skills/`

重启 WorkBuddy 后生效。

## 什么是 Skill

Skill 是给 AI 助手加载的专业知识包：一个 `SKILL.md` 定义触发条件与工作流程，`references/` 存放按需加载的细节文件。加载后助手会按既定流程工作，而不是即兴发挥。

本仓库技能遵循 Agent Skills 规范：YAML frontmatter + Markdown 正文 + 渐进式披露的 references。

## 许可

MIT License，见 [LICENSE](LICENSE)。
