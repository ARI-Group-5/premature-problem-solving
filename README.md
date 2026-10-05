# Detecting Premature Problem Solving in Mental Health Counseling Responses

## Project Overview

This project creates a new human-labeled dataset for detecting premature problem solving in mental-health counseling responses. Given a written **Context** and corresponding **Response**, annotators determine whether the response moves into advice, instructions, diagnosis, treatment, or other solution-directed guidance before adequately acknowledging the person’s emotional concern.

The resulting machine-learning task is binary text classification:

- **YES:** Solution-directed guidance occurs before adequate acknowledgment.
- **NO:** The response adequately acknowledges the emotional concern first, or remains exploratory without prematurely moving into a solution.

**SKIP** is available during annotation when an item cannot be labeled reliably or an annotator does not wish to continue with distressing content. SKIP is an annotation-process option and is not currently one of the model’s prediction classes.

This project evaluates response sequence only. It does not assess diagnosis, clinical quality, treatment safety, counselor competence, or whether the advice is correct.

## Dataset Access

- **Unlabeled annotation dataset:** [ADD GOOGLE DRIVE LINK]
- **Source repository:** [arafatanam/Mental-Health-Couseling](https://huggingface.co/datasets/arafatanam/Mental-Health-Couseling)
- **Original dataset:** [Amod/mental_health_counseling_conversations](https://huggingface.co/datasets/Amod/mental_health_counseling_conversations)
- **Date downloaded:** [ADD DATE]
- **Dataset revision or commit, if available:** [ADD REVISION OR “NOT RECORDED”]

The Google Drive link is configured so that University of Michigan students with the link can access the annotation data.

## Source and Provenance

The project uses the cleaned `arafatanam/Mental-Health-Couseling` dataset. The cleaned repository contains approximately 2,752 English Context–Response pairs and identifies the `Amod/mental_health_counseling_conversations` dataset as its original source.

The original dataset contains publicly available mental-health counseling question-and-answer pairs. According to its documentation, personally identifying information was removed before publication. Our team did not scrape or collect additional counseling conversations.

The source dataset does not contain the project’s premature-problem-solving target label. Our team and external annotators will create that label through human annotation.

## What Each Record Represents

Each record represents one written counseling exchange:

| Field | Description |
|---|---|
| `item_id` | Unique identifier created by the project team |
| `context` | The concern, question, or situation described by the person seeking support |
| `response` | The corresponding counseling response |

The unlabeled Potato input does not contain human labels, model predictions, or the team’s calibration results.

## Data Preparation

The team prepared the annotation dataset using the following process:

1. Downloaded the cleaned source dataset from Hugging Face.
2. Retained the original Context and Response text without rewriting it.
3. Checked for missing Context or Response values.
4. Checked for exact duplicate Context–Response pairs.
5. Identified Contexts that appear with multiple Responses.
6. Assigned each retained record a unique project item ID.
7. Selected an annotation subset using [DESCRIBE RANDOM-SAMPLING METHOD AND RANDOM SEED].
8. Removed or excluded [DESCRIBE EXCLUSIONS, IF ANY].
9. Exported an unlabeled file containing only `item_id`, `context`, and `response`.

## Dataset Statistics

| Measurement | Result |
|---|---:|
| Source records | 2,752 |

## Annotation Timing and Workload

Five team members independently labeled the same 20 calibration items. Together, they completed 100 judgments in 101 minutes.

- Average time per judgment: approximately **60.6 seconds**
- Estimated judgments per person-hour: approximately **59**
- Unanimous cases: **11 of 20**
- Cases with 4–1 agreement: **3 of 20**
- Cases with 3–2 agreement: **6 of 20**
- Average pairwise agreement: approximately **76%**

The annotation request contains:

- **Shared agreement set:** [ADD COUNT] items labeled by all assigned annotators
- **Distributed remainder:** [ADD COUNT] additional items assigned across annotators
- **Expected session length:** approximately one hour per annotator

The shared set will support inter-annotator agreement analysis and majority-label creation. The distributed remainder increases dataset coverage.

## Annotation Guidelines

Complete annotation instructions are available in [`annotation-guidelines.md`](annotation-guidelines.md).

Annotators judge only the Context and Response displayed in the interface. They must not assume that acknowledgment occurred during earlier conversation turns that are not included.

Advice alone does not automatically produce a YES label. The annotator evaluates the sequence in which acknowledgment and problem solving appear.

## Annotation Interface

The project uses [Potato](https://github.com/davidjurgens/potato), an open-source annotation platform developed for structured annotation tasks.

Potato presents one Context–Response pair at a time and records:

- Item ID
- Annotator ID
- YES, NO, or SKIP selection
- Notes or SKIP reason

Setup and usage instructions are available in [`potato/setup-instructions.md`](potato/setup-instructions.md).

## Sensitive Content and Annotator Well-Being

The dataset may contain discussions of depression, anxiety, trauma, abuse, self-harm, suicide, relationship conflict, and other distressing experiences.

Annotators may:

- Take breaks at any time
- Skip an item without penalty
- Stop annotating if they become uncomfortable
- Contact the project team with questions or concerns

The team will document how crisis and self-harm cases are handled before external annotation begins.

## Licensing

The cleaned `arafatanam/Mental-Health-Couseling` repository displays an Apache-2.0 license. However, the underlying `Amod/mental_health_counseling_conversations` dataset uses RAIL-D terms.

For this project, the team will treat the underlying Context and Response text as governed by the original RAIL-D terms and use it only for noncommercial academic research. The team will not assume that the source text can be redistributed under Apache-2.0.

Until redistribution rights are confirmed, the team will not publicly republish the complete source text with its annotations. The team’s original code, configuration, documentation, and annotation labels may be licensed separately where permitted.

## Changes From the Proposal

A summary of refinements made after instructor feedback and internal calibration is available in [`changes-from-proposal.md`](changes-from-proposal.md).

Major changes include:

- Adding the visible-context-only rule
- Clarifying that advice after acknowledgment can still receive NO
- Adding SKIP and annotator content safeguards

## Project Team

- MD Sirajum Muneer
- William Elder
- Octavio Clamont Bello
- Luke Stemmerich
- Sean Syversen

## Contact

Questions about the annotation task or technical problems should be directed to:

**[ADD CONTACT NAME]**  
**[ADD UMICH EMAIL OR APPROVED CONTACT METHOD]**
