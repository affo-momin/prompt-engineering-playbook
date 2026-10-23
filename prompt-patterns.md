# Prompt patterns

Each pattern shows a weak prompt, a stronger prompt, and why the stronger one works.
Text in `[brackets]` is a placeholder for you to fill in.

---

## 1. Role + audience

**Weak:** `Explain inflation.`

**Better:**
```
You are a patient economics teacher. Explain inflation to a 15-year-old in India
in under 150 words, using one everyday example with rupee amounts.
```

**Why:** The role sets the tone and expertise. The audience sets the vocabulary. The limit stops rambling.

---

## 2. Explicit output format

**Weak:** `Compare iPhone and Pixel cameras.`

**Better:**
```
Compare the main cameras of [phone A] and [phone B].
Return a markdown table with columns: Feature | [phone A] | [phone B] | Winner.
Cover: sensor size, low-light, video, zoom. End with a one-line verdict.
```

**Why:** A fixed structure makes answers easy to scan and easy to compare across models.

---

## 3. Few-shot examples

**Weak:** `Classify the sentiment of these reviews.`

**Better:**
```
Classify each review as positive, negative or neutral.

Review: "Arrived on time, works perfectly." -> positive
Review: "Battery died after two days." -> negative
Review: "It's a phone case." -> neutral

Review: "[review 1]" ->
Review: "[review 2]" ->
```

**Why:** The examples show the label set and the exact output style, so the model's labels stay consistent.

---

## 4. Step-by-step reasoning

**Weak:** `Is this invoice total correct?`

**Better:**
```
Check whether the invoice total below is correct.
First list each line item with quantity x price. Then add them, apply the [18]% tax,
and compare with the stated total. Finish with "CORRECT" or "INCORRECT: off by [amount]".

[invoice text]
```

**Why:** Asking for the working makes arithmetic errors visible and easier to check.

---

## 5. Constraints and guardrails

**Weak:** `Write a product description.`

**Better:**
```
Write a 60-80 word product description for [product].
Do not invent features that aren't in the spec below. Avoid the words "revolutionary" and "best".
If a detail is missing from the spec, leave it out rather than guessing.

Spec: [spec]
```

**Why:** The negative instructions and the "don't guess" rule cut down on hallucinated claims.

---

## 6. Decompose a big task

**Weak:** `Write a full training guide for new annotators.`

**Better (turn 1):**
```
Draft an outline (headings only) for a training guide for new data annotators on a
sentiment-labeling project. Max 8 sections.
```
**Better (turn 2):** `Now write section 3 in full, with two worked examples.`

**Why:** Reviewing the outline first catches structure problems before you spend effort on the details.

---

## 7. Self-check

**Weak:** `Summarise this article.`

**Better:**
```
Summarise the article in 5 bullets. Then add a section "Possible gaps" listing anything
important the summary leaves out and any claim you weren't sure about.

[article]
```

**Why:** The model flags its own weak spots, which saves the reviewer time.

---

## 8. Grounding in provided text

**Weak:** `What is our refund policy?`

**Better:**
```
Answer using ONLY the policy text below. Quote the sentence you relied on.
If the answer is not in the text, reply "Not covered in the policy."

Policy: [policy text]
Question: [question]
```

**Why:** Quoting the source and allowing "not covered" stops the model from making up a policy.
