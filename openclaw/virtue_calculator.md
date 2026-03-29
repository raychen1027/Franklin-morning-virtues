# 富兰克林准则 ISO 周数计算参考

## 快速计算表

| ISO 周数 | 计算 | 索引 | 准则 | 英文名 | 英文原文 |
|---------|------|------|------|--------|----------|
| 1 | (1-1)%13 | 0 | 节制 | TEMPERANCE | Eat not to dullness; drink not to elevation. |
| 2 | (2-1)%13 | 1 | 缄默 | SILENCE | Speak not but what may benefit others or yourself; avoid trifling conversation. |
| 3 | (3-1)%13 | 2 | 秩序 | ORDER | Let all your things have their places; let each part of your business have its time. |
| 4 | (4-1)%13 | 3 | 决心 | RESOLUTION | Resolve to perform what you ought; perform without fail what you resolve. |
| 5 | (5-1)%13 | 4 | 节俭 | FRUGALITY | Make no expense but to do good to others or yourself; i.e., waste nothing. |
| 6 | (6-1)%13 | 5 | 勤奋 | INDUSTRY | Lose no time; be always employ'd in something useful; cut off all unnecessary actions. |
| 7 | (7-1)%13 | 6 | 真诚 | SINCERITY | Use no hurtful deceit; think innocently and justly, and, if you speak, speak accordingly. |
| 8 | (8-1)%13 | 7 | 正义 | JUSTICE | Wrong none by doing injuries, or omitting the benefits that are your duty. |
| 9 | (9-1)%13 | 8 | 中庸 | MODERATION | Avoid extremes; forbear resenting injuries so much as you think they deserve. |
| 10 | (10-1)%13 | 9 | 清洁 | CLEANLINESS | Tolerate no uncleanliness in body, clothes, or habitation. |
| 11 | (11-1)%13 | 10 | 宁静 | TRANQUILITY | Be not disturbed at trifles, or at accidents common or unavoidable. |
| 12 | (12-1)%13 | 11 | 节欲 | CHASTITY | Rarely use venery but for health or offspring, never to dullness, weakness, or the injury of your own or another's peace or reputation. |
| 13 | (13-1)%13 | 12 | 谦逊 | HUMILITY | Imitate Jesus and Socrates. |
| 14 | (14-1)%13 | 0 | 节制 | TEMPERANCE | ... |
| 15 | (15-1)%13 | 1 | 缄默 | SILENCE | ... |
| ... | ... | ... | ... | ... | ... |

## 计算公式

```python
virtue_index = (iso_week - 1) % 13

# 例如：
# 第 1 周: (1-1) % 13 = 0 → 节制
# 第 13 周: (13-1) % 13 = 12 → 谦逊
# 第 14 周: (14-1) % 13 = 0 → 节制（新一轮）
```

## 手动查找方法

如果你无法使用脚本，可以：

1. **确定今天的 ISO 周数**
   - 使用在线工具：https://www.epochconverter.com/weeks/2026
   - 或使用日历应用查看当前周数

2. **计算索引**
   - 周数减 1
   - 除以 13，取余数
   - 余数即为索引（0-12）

3. **查找对应准则**
   - 索引 0 → 节制
   - 索引 1 → 缄默
   - ...
   - 索引 12 → 谦逊

## 2026 年周数对照表（部分）

| 日期 | ISO 周数 | 索引 | 准则 |
|------|---------|------|------|
| 2026-01-05 | 2 | 1 | 缄默 |
| 2026-01-12 | 3 | 2 | 秩序 |
| 2026-01-19 | 4 | 3 | 决心 |
| 2026-01-26 | 5 | 4 | 节俭 |
| 2026-02-02 | 6 | 5 | 勤奋 |
| 2026-02-09 | 7 | 6 | 真诚 |
| 2026-02-16 | 8 | 7 | 正义 |
| 2026-02-23 | 9 | 8 | 中庸 |
| 2026-03-02 | 10 | 9 | 清洁 |
| 2026-03-09 | 11 | 10 | 宁静 |
| 2026-03-16 | 12 | 11 | 节欲 |
| 2026-03-23 | 13 | 12 | 谦逊 |
| 2026-03-30 | 14 | 0 | 节制 |

---

**提示**：每年大约有 52 周，52 % 13 = 0，所以每年会完整循环 4 轮。
