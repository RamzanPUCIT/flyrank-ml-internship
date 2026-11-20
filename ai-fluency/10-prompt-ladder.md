# The Prompt Ladder

**Task:** a LinkedIn post about my FlyRank ML capstone. Outputs below were generated with Claude (excerpts).

| Ver | Prompt change | Output excerpt | What changed | Why | Better | Still weak |
|---|---|---|---|---|---|---|
| 0 (baseline) | "Write a LinkedIn post about my internship." | "Thrilled to announce I completed my internship at an amazing company…" | — | baseline | — | generic, no facts |
| 1 | + role & facts: ML intern, 18k pages, 81% vs 63% | "During my ML internship I ranked 18,000 pages…" | added facts | facts beat adjectives | specific | flat opening |
| 2 | + audience: hiring managers in data/ML | "If you hire data scientists, here's how I test models…" | audience named | relevance | speaks to reader | still long |
| 3 | + format: hook line, ≤ 180 words, 3 bullet lessons | "My Random Forest lost to a 3-line rule. 👇" | structure | scannable feed | strong hook | tone a bit salesy |
| 4 | + voice card: plain words, numbers next to baseline, no hype words | "A simple rule was right 81% of the time (random: 63%)." | voice | sounds like me | honest | CTA missing |
| 5 | + CTA + constraints: end with a question, 3–5 hashtags, link in comments | "…when did a simple rule beat your model? 👇 #MachineLearning" | CTA | engagement | complete | — |

**Final reusable prompt**
> You are helping an ML engineer write a LinkedIn post for hiring managers in data/ML. Facts: {facts with numbers and
> baselines}. Start with a one-line surprising hook, max 180 words, 3 short lessons as bullets, plain words, every number
> next to its baseline, no hype words, end with one question, 3–5 hashtags, say "link in comments".
