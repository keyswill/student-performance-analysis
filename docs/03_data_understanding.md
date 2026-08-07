# Phase 3: Data Understanding

**Status: Complete**

This phase explains the grain of each dataset, how the tables relate, which fields answer the business questions, and where the data limits interpretation.

## Dataset Structure

The project uses five related synthetic datasets. They do not share one grain and should not be flattened without controlling for duplication.

| Dataset | Grain | Records | Business use |
|---|---|---:|---|
| Student master | One row per student | 120 | Demographic and program context |
| Test scores | One row per student per quarter | 480 | Academic performance trends |
| Attendance | One row per student per quarter | 480 | Attendance monitoring |
| Behavior incidents | Aggregated student behavior records | 863 incidents | Behavioral context |
| Interventions | One row per intervention record | 119 | Support history and recorded outcomes |

## Keys and Relationships

`Student ID` is the common student identifier. The student table is the one-side of the relationship; scores, attendance, behavior, and interventions can contain multiple records for a student.

Because the tables have different grains, measures should be calculated within their source table or with controlled Tableau relationships. A direct many-to-many join could inflate grades, attendance, incidents, or intervention counts.

## Field Roles

### Primary analytical fields

- Student and quarter identifiers
- Quarter grade and performance level
- Days present, days absent, and attendance rate
- Incident count and behavior category
- Intervention focus area and outcome

### Context fields

- Grade level
- Race/ethnicity and gender
- IEP and ELL indicators
- Student name for the simulated detail view

### Fields needed for stronger future analysis

- Unique incident ID and event date
- Intervention start and end dates
- Intervention dosage and attendance
- Pre-intervention baseline and post-intervention measures

## Connection to Business Questions

| Business question | Required data | Planned measure | Interpretation limit |
|---|---|---|---|
| How is performance changing? | Scores, quarter, grade level | Average quarter grade | Averages can hide individual variation |
| Is attendance associated with grades? | Attendance and scores at student-quarter grain | Correlation and attendance-group comparison | Association is not causation |
| Which students need review? | Scores, attendance, behavior, interventions | Multi-signal student profile | Human judgment remains necessary |
| Are subgroup patterns different? | Student master and scores | Quarterly subgroup averages and counts | Small groups limit generalization |
| Which interventions show positive outcomes? | Intervention focus and outcome | Positive-outcome share | Selection effects prevent effectiveness claims |

## Validated Baseline

| Metric | Value |
|---|---:|
| Students | 120 |
| Average quarter grade | 80.28 |
| Overall attendance rate | 90.72% |
| Behavior incidents | 863 |
| Students with an intervention | 45 |

Quarterly attendance and grade have a Pearson correlation of 0.507. Records below 85% attendance average 70.39, compared with 82.75 for records at or above 85%. This supports attendance as a review signal, not as proof of cause.

## Quality and Interpretation Risks

- IEP and ELL groups contain 20 and 21 students, respectively.
- Intervention records are not randomly assigned and lack dosage.
- Behavior records cannot support reliable incident timing analysis.
- A student can appear in multiple child tables, creating duplication risk.
- The dashboard contains simulated names and records only.

## Analytical Readiness

The data is suitable for descriptive trend analysis, subgroup monitoring, and individual-record review. It is not sufficient for causal intervention evaluation, automated risk scoring, or claims about real student populations.

## Related Documentation

- [Data dictionary](../data/data-dictionary.md)
- [Validated analysis](validated-analysis.md)
- [Phase 2 Business Understanding](02_business_understanding.md)

