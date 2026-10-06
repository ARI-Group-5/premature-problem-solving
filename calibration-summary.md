# Internal Calibration Results

*Premature Problem-Solving Annotation Task — Phase 1*

> **Interpretation note:** These results describe internal calibration, not final ground-truth labels or the project's final inter-annotator agreement.

## Purpose

This preliminary calibration tested whether five team members could apply the draft annotation rules consistently before external annotation begins. The results support the task's feasibility while identifying decision rules that still require adjudication.

## Calibration method

Five annotators independently labeled the same 20 Context–Response pairs without reviewing one another's answers. Each annotator selected **YES**, **NO**, or **SKIP**, producing **100 independent judgments**.

### Label definitions used for this report

| Label | Operational meaning |
|---|---|
| **YES** | The response moves into advice, instructions, recommendations, diagnosis, or other solution-directed guidance **before** adequately acknowledging the expressed emotional concern. |
| **NO** | The response adequately acknowledges the concern before problem-solving, or remains exploratory without prematurely moving to a solution. |
| **SKIP** | The case cannot reasonably be labeled under the current rules or should not be labeled because of content concerns; the annotator records a reason. |

## Agreement results

The team reached unanimous agreement on **11 of 20 cases (55%)**. Three cases had 4–1 agreement, and six had a 3–2 split. In total, **14 of 20 cases (70%)** received agreement from at least four annotators.

| Agreement pattern | Cases | Share of cases |
|---|---:|---:|
| Unanimous (5–0) | 11 | 55% |
| 4–1 split | 3 | 15% |
| 3–2 split | 6 | 30% |

**Raw pairwise agreement was 76%.** This equals 152 matching annotator-pair decisions out of 200 possible pair comparisons across the 20 cases. SKIP was treated as a distinct category. This descriptive statistic is not chance-corrected and should not be reported as Krippendorff's alpha.

| Label | Judgments | Share |
|---|---:|---:|
| YES | 39 | 39% |
| NO | 60 | 60% |
| SKIP | 1 | 1% |

## What drove disagreement

The nine non-unanimous cases were not random. Disagreement clustered around the threshold for **adequate acknowledgment** and the handling of special cases. Recurring questions included:

- whether recognizing symptoms counts as emotional acknowledgment;
- whether indirect language such as *“it sounds like”* provides sufficient validation;
- whether normalization, causal explanations, or praise for seeking help count as acknowledgment;
- how much acknowledgment is sufficient before a response moves into advice; and
- how urgent safety guidance should be handled in crisis or self-harm examples.

These patterns show that the task requires judgment about acknowledgment quality and response sequence; it is not reducible to keyword detection. They also provide concrete targets for the next guideline revision.

## Annotation timing and workload

| Measure | Result |
|---|---:|
| Annotators | 5 |
| Cases per annotator | 20 |
| Total judgments | 100 |
| Combined annotation time | 101 minutes |
| Average time per annotator | 20.2 minutes for 20 cases |
| Average time per judgment | 60.6 seconds |
| Approximate throughput | 59 judgments per person-hour |

If the team retains the proposed target of **1,200 records with two independent annotations per record**, the observed pace implies approximately **40.4 person-hours of labeling**. This estimate excludes calibration, adjudication, breaks, quality review, and interface overhead, so it should be treated as a lower-bound planning estimate rather than a delivery commitment.

## Conclusion and next steps

The calibration supports moving forward, but the draft rules should not yet be treated as final. Before external annotation begins, the team should:

1. Review and adjudicate the nine non-unanimous cases.
2. Document explicit decisions for indirect acknowledgment, normalization, causal explanations, praise for help-seeking, crisis guidance, and SKIP usage.
3. Assign a final adjudicated label or exclusion decision to each calibration case.
4. Freeze the revised rules as **Annotation Guidelines Version 1.0**.
5. Test the frozen guidelines and Potato interface end to end before releasing the primary annotation task.

**Bottom line:** The team achieved 76% raw pairwise agreement, but the nine non-unanimous cases show that the definition of adequate acknowledgment must be operationalized more precisely before full-scale annotation.
