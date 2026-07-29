# Validated Analysis and Claim Review

This document reconciles the public case-study claims to the five CSV files.

## Headline Metrics

| Metric | Validated Value |
| --- | ---: |
| Students | 120 |
| Quarterly score records | 480 |
| Quarterly attendance records | 480 |
| Average quarter grade | 80.28 |
| Overall attendance rate | 90.72% |
| Behavior incidents | 863 |
| Intervention records | 119 |
| Students with an intervention | 45 |

## Quarterly Average Grade

| Quarter | Average |
| --- | ---: |
| Q1 | 79.18 |
| Q2 | 80.05 |
| Q3 | 80.83 |
| Q4 | 81.05 |

## Attendance Relationship

The Pearson correlation between quarterly attendance rate and quarterly grade is
0.507. This is a moderate positive association.

| Attendance Group | Records | Average Grade |
| --- | ---: | ---: |
| Below 85% | 96 | 70.39 |
| At or above 85% | 384 | 82.75 |

The difference is 12.37 points. This supports using attendance as a review
signal, but it does not establish that attendance is the single strongest
predictor because no multivariable predictive model was tested.

## Subgroup Context

- IEP: 20 Yes and 100 No
- ELL: 21 Yes and 99 No

IEP students averaged 82.54 in Q1, 80.68 in Q2, 82.92 in Q3, and 83.42 in Q4.
The pattern supports a Q2 review point. It does not prove that IEP services
caused the rebound.

ELL students averaged 79.72 in Q1, 80.80 in Q2, 82.34 in Q3, and 79.72 in Q4.
The Q4 change warrants investigation. The dataset does not contain curriculum
complexity or language-support intensity, so it cannot explain the decline.

## Intervention Outcomes

Positive outcome is defined as Improving or Exited - Met Goal.

| Focus Area | Records | Positive | Positive Share |
| --- | ---: | ---: | ---: |
| Academic | 28 | 19 | 67.9% |
| Attendance | 30 | 14 | 46.7% |
| Behavioral | 32 | 13 | 40.6% |
| Social-Emotional | 29 | 14 | 48.3% |

Academic-focus records have the highest positive share in this simulated
dataset. Selection effects, different student needs, and missing intervention
dosage prevent a causal effectiveness conclusion.

## Corrections to the Original Narrative

| Original Framing | Defensible Revision |
| --- | --- |
| Attendance is the single strongest predictor | Attendance has a moderate positive association with grades and is a useful review signal |
| IEP supports deliver results | IEP students dip in Q2 and recover in Q3-Q4; causes are not measured |
| ELL decline proves a Q4 language-support gap | ELL students decline in Q4; curriculum and support data are needed to explain why |
| Academic interventions produce the highest return | Academic-focus records have the highest positive-outcome share; effectiveness is not established |
| Routines caused the post-Q2 incident decline | Incidents decline after Q2; the dataset does not measure the cause |
