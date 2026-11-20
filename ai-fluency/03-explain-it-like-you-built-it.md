# Explain It Like You Built It

**The piece:** the baseline score in my refresh queue (`w04_baseline_score.ipynb`).

Every page gets three numbers from the *earlier* 30 days only: how new it is, how weak its click-through rate was,
and how much search demand it already had. Each number is turned into a 0–1 rank against all other pages, then
mixed: 40% "young", 40% "weak CTR", 20% "demand". Pages are sorted by that mix, and each gets one reason code
(e.g. `ZERO_CLICK_YOUNG_PAGE`) that maps to one action (e.g. "rewrite title and meta").

**Why built this way:** an editor must understand why a page is on the list. On sites it never saw, this simple
rule got about 81% of its top 50 right versus 63% by chance, and two machine-learning models did not beat it.
I deliberately never use anything from the latest 30 days as input, because that is the window the answer comes from.
