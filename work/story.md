# ML-12 — Tell the Story

## Case-study framing (also on the deployed paper)
FlyRank publishes and refreshes content for many client sites. Editors can review only a few pages a week, so the
real problem is **ordering**: which pages first? This project turns 18k pages from 30 anonymized sites into a
per-client review queue with one reason code and one action per page. Measured on sites the method never saw, the
top 50 pages had a demand drop ~81% of the time vs a ~63% base rate. A transparent three-signal rule beat
learned models, so the rule is what ships — as decision-support, not automation.

## 5-minute demo outline
1. **0:00–0:45 Problem** — hundreds of pages per client, a few review slots per week.
2. **0:45–1:30 Data & label** — earlier 30 days as inputs, later 30 days as the observed outcome; what was excluded and why.
3. **1:30–2:30 Baseline** — two signal checks (CTR confirmed, staleness mixed, age opposite); the rule and reason codes.
4. **2:30–3:30 Model vs baseline** — grouped-by-client CV table; random split inflates AUC 0.60 → 0.70; rule wins top-50.
5. **3:30–4:30 Playbook** — top-10 per client, actions, human checks, no-go list, retrain triggers.
6. **4:30–5:00 Limits** — directional, no causal claim, weak on 365+ pages; link to paper and repo.

## Cut 1 — LinkedIn post
In the FlyRank ML internship I tried to answer a practical question: which pages should an editor refresh first?
I compared a simple three-signal rule with Logistic Regression and Random Forest on 18k anonymized pages, testing
only on client sites the models never saw. The honest result: the simple rule ranked best at the top of the queue
(precision@50 ≈ 0.81 vs 0.63 base rate). Complexity has to earn its place. Paper: https://ramzanpucit.github.io/flyrank-ml-internship/
Built on the FlyRank ML Internship dataset — flyrank.ai

## Cut 2 — one-paragraph summary
A per-client refresh queue built from earlier-window signals (page age, earlier CTR, earlier demand) picks pages that
go on to lose demand ~81% of the time in its top 50, versus ~63% at random, on held-out sites. Learned models did
not improve on it. Use it to decide where to look first; it does not prove a refresh will recover traffic.
