# Module 7 Integrated Evaluation Report — Fine-Tuning vs. Pre-Trained Inference

> Written by [your name removed for privacy] for the Module 7 deliverable.
> Synthesizes Lab 7A (fine-tuning), Integration 7A (domain shift), Lab 7B (QA), and Integration 7B (summarization).
>
> **Replace this template's placeholders with your numbers and analysis. Each of the six sections below is required.**

---

## 1. Comparison Table

Paste your numbers from `metrics.json` (Lab 7A), `qa_metrics.json` (Lab 7B), and `summary_metrics.json` (this integration). The TA cross-checks that these match your submitted files.

| Task | Approach | Model | Training cost | Inference cost | Quality metric | Value |
|---|---|---|---|---|---|---|
| Sentiment classification (Lab 7A) | Fine-tuning | DistilBERT | ~30 min CPU + 3K labels | ~50 ms / example | Macro-F1 | _(your number)_ |
| Domain transfer (Integration 7A) | Fine-tuned model out-of-domain | (same) | already trained | ~50 ms / example | Domain-shift judgment | _(qualitative)_ |
| Extractive QA (Lab 7B) | Pre-trained inference | distilbert-base-cased-distilled-squad | 0 | ~50 ms / example | EM / token-F1 | _(your numbers)_ |
| Summarization (Integration 7B) | Pre-trained inference | distilbart-cnn-6-6 | 0 | ~3 sec / example | ROUGE-1 / 2 / L F1 | _(your numbers)_ |

## 2. Findings

3–5 bullet points characterizing what each approach excels at and where it breaks. Tied to your specific numbers.

- _(finding 1)_
- _(finding 2)_
- _(finding 3)_

## 3. Faithfulness Check

Pick three summaries from `summary_predictions.csv` (one high-ROUGE, one mid-ROUGE, one low-ROUGE). For each:

- Quote the article excerpt and the predicted summary.
- Mark whether the summary is faithful (every claim in the summary appears in the article).
- Comment on what ROUGE caught or missed for this case.

### Example A — high ROUGE

> Article excerpt: _(quote)_
> Predicted summary: _(quote)_
> ROUGE-1: _(value)_; ROUGE-2: _(value)_; ROUGE-L: _(value)_
> Faithful? _(yes/no + brief commentary)_

### Example B — mid ROUGE

_(same structure)_

### Example C — low ROUGE

_(same structure)_

## 4. Production Decision Matrix

For each scenario, recommend fine-tuning or pre-trained inference. **Justify with one specific sentence tied to your measured numbers.**

| Scenario | Recommendation | Justification |
|---|---|---|
| Real-time app store review triage dashboard for a product team | _(your call)_ | _(your justification)_ |
| Daily tech / entertainment news summary digest for an internal newsroom | _(your call)_ | _(your justification)_ |
| Domain-expert QA on legal contracts | _(your call)_ | _(your justification)_ |

## 5. What You Would Do Differently

One paragraph on what you would change about your approach if you had a labeled summarization dataset for the tech/entertainment news domain. Be concrete — what investment would meaningfully change the numbers?

_(your paragraph)_

## 6. Limits of the Evaluation

One paragraph on what these numbers do **not** tell you. Faithfulness, calibration, latency under load, etc. Pick the limits that matter most for the production scenarios in Section 4.

_(your paragraph)_
