# Coaching-Me Skill

> An adaptive AI coaching framework — turns AI into a Socratic coach

## Origin Story

This skill emerged from an observation: the best AI conversations aren't when AI gives answers — it's when AI asks the right questions.

## The Insight

A YouTube video by mrblock (區塊先生) showed a powerful technique:

> Instead of asking ChatGPT questions, tell it your problem and ask it to ask YOU questions — one at a time.

This transforms AI from an answer engine into an **executive coach** that helps you think, rather than thinks for you.

## Design Discussion

### Initial Concept

**User's question**: "What's the principle behind this?"

The insight was recognized as:
1. **Socratic Method** — ancient teaching technique of asking questions to lead to self-discovery
2. **Constructivism** — people actively build knowledge through reflection
3. **Coaching Leadership** — powerful questions as a catalyst for thinking

### Time Framework Debate

**Initial thought**: How long should a coaching session last?

**Proposed breakdown**:
| Type | Duration |
|------|----------|
| Micro | 3-5 minutes |
| Standard | 10-20 minutes |
| Deep | 30-60 minutes |

### The Adaptive Framework

User (George) proposed a self-regulating system:

> "Start with standard, then if questions exceed 20 or responses are slow (>1-2min per question), compress to micro. If it's fast and flowing, extend to deep."

This became the **adaptive mode switching logic** we implemented.

### The Key Realization

```
"Coach me [target]"
```

Understood as: "Guide me through understanding [topic] using questions"

### Session Output Debate

User asked: "What about evaluation/recommendations at the end?"

**Final decision**: Yes, session should output:
1. **Detailed conversation summary** — full Q&A log
2. **Evaluation scores** — clarity, depth, action readiness
3. **Recommendations** — immediate actions + follow-up topics

### Publishing Decision

User decided to:
1. Build the skill as `coaching-me`
2. Write the README documenting the design discussion
3. Publish to GitHub

## Key Design Principles

1. **User constructs understanding, not passive recipient**
2. **AI is a thinking coach, not an answer provider**
3. **Mode adapts to conversation flow, not predetermined**
4. **Always end with actionable output**
5. **No judgment mid-session — stay neutral**

## Files

- `SKILL.md` — Complete skill specification
- `README.md` — This document (design history)
- `sessions/` — Saved coaching session summaries (created at runtime)

## Usage

```
coach me negotiation strategies
coach me 我的定價策略
教練模式 職涯選擇
done (to end and get summary)
```

## Related Skills

- **[Learn-With-Coach](https://github.com/arbiger/learn-with-coach)** — AI 學習教練，用 3 步驟執行迴圈學會任何技能
- **[KB-Collector](https://github.com/arbiger/kb-collector)** — Knowledge base collection with AI summarization
- **[Valuation-Calculator](https://github.com/arbiger/valuation-calculator)** — Fast stock valuation tools

## 與 Learn-With-Coach 的整合 Integration with Learn-With-Coach

```
coaching-me (discovery + questioning)
        ↓ (triggers when interest found)
「這個很有趣，要不要多了解？」
        ↓ (yes)
learn [topic] (execution + structure)
        ↓ (if stuck, use coaching questions)
coaching-me (deeper exploration)
        ↓ (complete phase)
Phase summary
        ↓ (continue or close)
```

**使用範例 Example:**
```
User: [在 coaching-me 對話中]
     「我最近對機器學習很有興趣」
     
AI: 很有趣！你對 ML 的興趣讓我想到...
    要不要建立一個學習計劃來深入了解？
    「learn machine learning」
```

## License

MIT — use freely, contribute improvements

---

*Built through collaborative design discussion, March 2026*
