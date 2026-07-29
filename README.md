# Student Performance Analytics

An interactive Tableau case study designed to help middle-school leaders identify
academic risk earlier by connecting grades, attendance, behavior, interventions,
and student-group context.

> **Data disclaimer:** Every student, name, identifier, score, attendance record,
> incident, and intervention in this project is fictional. The dataset was
> synthetically generated for portfolio use and contains no real student records
> or FERPA-protected information.

## Executive Summary

School data is often reviewed in separate systems and at different times. This
project combines five related datasets into three Tableau dashboards so that an
administrator can move from a school-wide trend to a subgroup pattern and then
to an individual student record.

The analysis covers 120 simulated students in Grades 6-8 across four quarters:

- 480 quarterly academic records
- 480 quarterly attendance records
- 863 behavior incident records
- 119 intervention records involving 45 students

The strongest actionable relationship is between attendance and academic
performance. Quarterly attendance and grades have a moderate positive
correlation of **0.507**. Students below 85% attendance averaged **70.39**, while
students at or above 85% averaged **82.75**, a **12.37-point difference**.

## Business Problem

Administrators need a repeatable way to answer four questions:

1. How is academic performance changing by quarter and grade?
2. Which observable signals are associated with lower performance?
3. Are outcomes different across IEP, ELL, or demographic groups?
4. Which students need review, and what support history already exists?

The dashboard is an early-warning and decision-support tool. It does not diagnose
causes or claim that an intervention produced a student's outcome.

## Stakeholders and Decisions

| Stakeholder | Decision Supported |
| --- | --- |
| Principal or assistant principal | Where to focus attendance and academic-review resources |
| Department or grade-level lead | Which grade-level or quarterly patterns need investigation |
| Teacher | Which students need a closer review of grades, attendance, and behavior |
| Counselor or intervention team | Whether prior supports and outcomes should inform the next action |

## Dashboard Suite

### 1. Quarterly Overview

Tracks average grades, attendance, proficiency levels, behavior incidents, and
grade-level trends. The attendance-versus-grade view highlights students whose
attendance and performance warrant review.

![Quarterly Overview dashboard](dashboard/quarterly-overview.png)

### 2. Equity and Subgroup Analysis

Compares quarterly performance for IEP and ELL groups, summarizes demographic
representation, and reviews intervention outcomes. Small subgroup sizes are
shown as context and should limit generalization.

![Equity and Subgroup Analysis dashboard](dashboard/equity-subgroup-analysis.png)

### 3. Individual Student Overview

Combines a selected student's grades, attendance, behavior history, and
interventions in one view. This supports investigation and conversation; it is
not an automated decision system.

![Individual Student Overview dashboard](dashboard/individual-student-overview.png)

[Download the packaged Tableau workbook](dashboard/Student%20Performance%20Dashboard.twbx)

## Validated Findings

1. **Grades improved modestly over the year.** The overall average rose from
   79.18 in Q1 to 81.05 in Q4.
2. **Attendance is associated with performance.** The quarterly correlation
   between attendance rate and grade is 0.507. The 85% attendance comparison
   shows a 12.37-point average-grade difference.
3. **Grade-level trends differ.** Grade 6 led in Q3 at 82.31, while Grade 8
   declined in Q2 before recovering to 79.86 in Q4.
4. **IEP and ELL patterns require cautious interpretation.** The simulated
   dataset contains only 20 IEP students and 21 ELL students. IEP students dip
   in Q2 and recover; ELL students rise through Q3 and fall in Q4. These are
   monitoring signals, not evidence of why the changes occurred.
5. **Academic-focus interventions had the highest positive-outcome share.**
   Nineteen of 28 academic-focus records were marked Improving or Exited - Met
   Goal (67.9%). Because interventions were not randomly assigned, this is an
   association and not proof of effectiveness.

## Recommendations

- Use attendance below 85% as a review trigger, then consider grades, behavior,
  and student context before choosing an action.
- Add a formal Q2 subgroup review because the simulated IEP trend changes most
  sharply in that quarter.
- Review the ELL Q4 decline with curriculum, assignment, and support data before
  attributing a cause.
- Track intervention start dates, duration, dosage, and pre/post measures so
  future analysis can evaluate change more rigorously.
- Add stable incident IDs and dates to improve behavior-data auditability.

## Tools and Skills Demonstrated

- **Primary tool:** Tableau
- Tableau data relationships across five tables
- Calculated fields, parameters, filters, LOD expressions, and dashboard actions
- KPI design, subgroup analysis, exploratory analysis, and data storytelling
- Stakeholder requirements and analytical guardrails

## Repository Guide

| Path | Contents |
| --- | --- |
| [`dashboard/`](dashboard/) | Packaged Tableau workbook, dashboard preview, and usage notes |
| [`data/`](data/) | Five CSV datasets, data dictionary, and relationship notes |
| [`docs/business-requirements.md`](docs/business-requirements.md) | Stakeholders, decisions, requirements, and acceptance criteria |
| [`docs/validated-analysis.md`](docs/validated-analysis.md) | Reconciled metrics, caveats, and claim corrections |

## Limitations

- The dataset is synthetic and intentionally demonstrates analytical workflow,
  not real-world prevalence or outcomes.
- The analysis is observational and descriptive.
- IEP and ELL subgroup sizes are small.
- Intervention records lack dosage and reliable pre/post comparison windows.
- Behavior records do not include event dates or unique incident identifiers.

## Author

Kiran Williams

[LinkedIn](https://www.linkedin.com/in/kiranwilliams/) |
[Portfolio](https://kiranwilliams.carrd.co)
