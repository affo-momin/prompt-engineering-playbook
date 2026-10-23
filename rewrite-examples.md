# Before / after prompt rewrites

| # | Before | Problem | After |
|---|---|---|---|
| 1 | `Write an email to my manager about leave.` | No dates, reason, tone or length | `Write a polite 4-sentence email to my manager asking for leave on [date-date] for [reason]. Mention my pending work is handed to [name].` |
| 2 | `Give me SQL to find duplicates.` | Unknown table and what "duplicate" means | `Table customers(id, email, phone, created_at). Write SQLite that lists emails appearing more than once, with a count, newest first.` |
| 3 | `Is this search result good for "pizza near me"?` | No rating scale or location | `Using a 0-4 relevance scale (0 = off-topic, 4 = perfect), rate this result for the query "pizza near me" from a user in [city]. Give the score and a one-line reason.` |
| 4 | `Summarise this.` | No length, audience or focus | `Summarise this report for a busy team lead in 3 bullets: the main finding, the biggest risk, and the next step.` |
| 5 | `Make this better.` | "Better" is undefined | `Rewrite this paragraph for clarity: shorter sentences, active voice, under 80 words, same meaning.` |
| 6 | `Translate to Hindi.` | Register and terminology unclear | `Translate to everyday spoken Hindi (not formal). Keep product names in English. Return only the translation.` |
| 7 | `List AI tools.` | Too broad | `List 5 free tools for labeling images for machine-learning datasets, with one line each on what makes it different.` |
| 8 | `Check my resume.` | No target role or criteria | `Review my resume for an "AI data quality specialist" role. Point out the 3 weakest bullets and rewrite each one with a clearer outcome.` |
