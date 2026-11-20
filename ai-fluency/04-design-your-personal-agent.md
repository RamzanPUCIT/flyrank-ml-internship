# Design Your Personal Agent — "Research Inbox Agent"

**Job:** every morning, collect new papers and notes for my M.Phil topic, summarize each in 5 lines, and add the
useful ones to a reading list with a one-line "why it matters to my thesis".

| Part | Design |
|---|---|
| Trigger | scheduled, weekdays 8:30 am |
| Inputs | saved search queries, a Google Drive "to-read" folder |
| Tools | web search (new papers), Drive (read PDFs, write the list), Gmail (send me a digest) |
| Steps | 1) search → 2) skip anything already on the list → 3) read abstract + conclusion → 4) 5-line summary + relevance score 1–5 → 5) append rows with score ≥ 3 → 6) send digest |
| Output | one Google Sheet row per paper + one short email |
| Human-in-the-loop | the agent never deletes or moves files and never emails anyone but me; I mark "read" myself |
| Failure points | paywalled PDFs (log and skip), duplicate titles (match on DOI), weak relevance scores (I review weekly and adjust the queries) |
| Success measure | ≥ 3 useful papers a week; under 10 minutes of my time to review the digest |
