# AI Methodology

## Classification

Tshwi Advisor is an **explainable, knowledge-based AI recommendation system**. It does not depend on a trained machine-learning classifier or a large language model to generate course matches.

## Recommendation pipeline

```text
Assessment Answers
       |
       v
Interest Signals
       |
       v
Weighted Interest Profile
       |
       v
Programme-domain Comparison
       |
       v
Specificity / Domain Discrimination
       |
       v
Normalised Match Scores
       |
       v
Ranked Top-3 Programmes
```

## Weighted interest profile

Assessment responses contribute signals to career-interest dimensions. These signals are aggregated into a weighted profile rather than treating every selected concept as equally informative.

## Knowledge base

Each programme is represented through curated career and interest-domain information. The recommendation engine compares the derived student profile with these programme characteristics.

## Domain discrimination

Broad interests such as technology can apply to many programmes. More discriminating signals—such as security, critical thinking, data analysis, creativity, business or people-focused interests—help distinguish programmes that otherwise share broad domains.

## Specificity

More specific alignment can receive greater influence than generic overlap. This reduces the risk that a broad interest dominates the ranking merely because it appears across many programmes.

## Deterministic inference

For the same knowledge base and the same assessment answers, the system produces the same recommendation result. This supports:

- reproducibility;
- auditability;
- regression testing;
- transparent debugging; and
- controlled refinement of recommendation rules.

## Explainability

The output is a **career-guidance recommendation**, not an admissions decision. Match percentages communicate relative alignment within the implemented knowledge model; they should not be interpreted as probabilities of academic success, employment or admission.

## Validation approach

Recommendation behaviour is tested with synthetic personas representing different interest profiles. End-to-end tests exercise the path from assessment answers through profile derivation to ranked programme output.

The production formula is treated as a controlled component: changes should be evidence-driven and regression-tested rather than made merely to alter individual results.
