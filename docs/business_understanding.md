# Business Understanding

**Status: Complete**

This document defines the school decision the analysis supports, the intended users, the measures needed, and the limits of what the synthetic data can establish.

## Business Context

School leaders often review grades, attendance, behavior, and intervention records in separate systems. That fragmentation makes it harder to identify students who may need support and to understand whether a school-wide trend is concentrated in a particular grade, quarter, or subgroup.

This project combines five synthetic datasets into a decision-support dashboard that moves from school-level trends to subgroup patterns and individual student context.

## Main Business Question

> How can school leaders combine academic, attendance, behavior, and intervention data to identify emerging risks and prioritize student reviews?

## Business Problem

An isolated low grade, absence, or behavior incident does not provide enough context for a support decision. Administrators need a repeatable way to review multiple signals together, recognize patterns earlier, and see what support has already been provided.

The dashboard is designed to improve the consistency and speed of that review. It is not an automated placement, discipline, or diagnostic system.

## Stakeholders

| Stakeholder | Decision supported |
|---|---|
| Principal or assistant principal | Prioritize attendance, academic, and intervention review resources |
| Grade-level or department leader | Identify quarters, grades, or subgroups requiring investigation |
| Teacher | Review a student's grades, attendance, behavior, and support history together |
| Counselor or intervention team | Consider prior supports and recorded outcomes before selecting the next action |

## Business Objectives

1. Monitor academic and attendance performance by quarter and grade.
2. Identify observable signals associated with lower academic performance.
3. Compare outcomes across IEP, ELL, and demographic groups with sample-size context.
4. Consolidate individual student records for human review.
5. Evaluate recorded intervention outcomes without overstating effectiveness.

## Success Metrics

| Metric | Definition | Decision supported |
|---|---|---|
| Average quarter grade | Mean quarterly grade in the selected context | Monitor academic performance |
| Overall attendance rate | Days present divided by total school days | Identify attendance-related review needs |
| Behavior incidents | Sum of recorded incident counts | Add behavioral context to student review |
| Students in intervention | Distinct students with an intervention record | Monitor support reach |
| Positive intervention outcome | Improving or Exited - Met Goal | Compare recorded outcomes by focus area |

## Business Questions

1. How do average grades and attendance change by quarter and grade?
2. What relationship is visible between attendance and academic performance?
3. Which students combine lower attendance with lower grades?
4. How do IEP and ELL trends vary across the year?
5. Which intervention focus areas have the highest recorded positive-outcome share?
6. What prior behavior and intervention history should a reviewer see before acting?

## Assumptions

- Every record is fictional and created for portfolio use.
- Student identifiers connect records across the five datasets.
- Quarterly academic and attendance records represent comparable reporting periods.
- Intervention outcomes are descriptive labels, not experimental evidence.
- Attendance, behavior, and grades are review signals rather than automatic decision rules.

## Risks and Limitations

| Limitation | Effect on the analysis | Treatment |
|---|---|---|
| Synthetic data | Results do not describe a real school | Use findings to demonstrate workflow only |
| Observational design | Relationships cannot establish causality | Use association language |
| Small IEP and ELL groups | Subgroup results may be unstable | Display counts and limit generalization |
| Missing intervention dosage and pre/post windows | Effectiveness cannot be tested rigorously | Report recorded outcomes only |
| Behavior records lack dates and unique incident IDs | Timing and auditability are limited | Recommend stronger future data collection |

## Main Limitation

> The dashboard helps people prioritize a closer review; it does not determine why a student is struggling or prescribe an intervention.

## Related Documentation

- [Business requirements](business-requirements.md)
- [Validated analysis](validated-analysis.md)
- [Data Understanding](data_understanding.md)
