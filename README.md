# ⚡ Pairwise Test Calculator

A free, browser-based pairwise (all-pairs) test case generator. No installation, no backend, no account required — just open and use.

🔗 **[Live Demo →](https://yourusername.github.io/pairwise-calculator)**

---

## What is Pairwise Testing?

When testing a system with multiple parameters, testing every possible combination (exhaustive testing) quickly becomes impractical:

| Parameters | Values each | Exhaustive combinations |
|---|---|---|
| 4 params | 3–5 values | ~120–625 test cases |
| 6 params | 3–5 values | ~729–15,625 test cases |

Pairwise testing solves this by ensuring **every combination of any two parameter values appears in at least one test case** — typically reducing test case count by **70–95%** while catching the vast majority of bugs.

> Research by Kuhn et al. (2004) found that ~85% of software faults are triggered by interactions of at most 2 parameters. Pairwise coverage is therefore a highly cost-effective baseline.

---

## Features

- 🌐 **Bilingual** — English / Turkish (toggle in the top-right corner)
- ⚡ **Instant results** — greedy algorithm runs entirely in the browser
- ✅ **Coverage verification** — confirms all parameter pairs are covered
- 📥 **CSV export** — ready to open in Excel or Google Sheets
- 📋 **One-click copy** — paste directly into any spreadsheet
- 📄 **PICT .model export** — use output with Microsoft's [PICT](https://github.com/microsoft/pict) CLI tool
- 🚀 **4 built-in examples** — AI Chatbot, Browser matrix, E-commerce checkout, ML configuration

---

## How to Use

1. Enter your parameter names and their possible values (comma-separated)
2. Click **"Calculate Pairwise"**
3. Review the generated test cases and coverage stats
4. Export to CSV or copy to clipboard

Or load one of the built-in examples to see it in action immediately.

---

## Example

**AI Chatbot configuration:**

| Parameter | Values |
|---|---|
| Language Model | LM1, LM2, LM3, LM4, LM5 |
| Response Tone | Formal, Semi-formal, Casual, Technical |
| Context Window | 2K, 4K, 8K |
| Safety Filter | Basic, Advanced |

- Exhaustive: **5 × 4 × 3 × 2 = 120 test cases**
- Pairwise: **~20 test cases** (~83% reduction)
- All 56 parameter pairs covered ✅

---

## Running Locally

No build step needed — it's a single HTML file.

```bash
git clone https://github.com/yourusername/pairwise-calculator.git
cd pairwise-calculator
open index.html   # macOS
# or just double-click index.html on any OS
```

---

## Algorithm

The generator uses a **greedy algorithm**: at each step, it selects the candidate test case that covers the most currently uncovered parameter pairs. This approach produces near-optimal results in practice and runs in milliseconds in the browser.

For large parameter spaces or advanced features (t-way coverage beyond 2, constraints), consider [Microsoft PICT](https://github.com/microsoft/pict).

---

## References

- Kuhn, D.R., Wallace, D.R., & Gallo, A.M. (2004). Software fault interactions and implications for software testing. *IEEE Transactions on Software Engineering, 30*(12), 418–421.
- Cohen, D.M., Dalal, S.R., Fredman, M.L., & Patton, G.C. (1997). The AETG system. *IEEE Transactions on Software Engineering, 23*(7), 437–444.
- Czerwonka, J. (2006). Pairwise testing in the real world. *Pacific Northwest Software Quality Conference.*
- [ISTQB CT-AI Syllabus v1.0](https://www.istqb.org) — recommends pairwise as the preferred combinatorial technique for AI system configuration testing.

---

## License

MIT — free to use, modify, and distribute.
