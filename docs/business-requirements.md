# Business Requirements

## Objective

Create a Tableau decision-support dashboard that integrates academic,
attendance, behavior, intervention, and demographic data so school leaders can
identify patterns and prioritize student reviews.

## Stakeholders

- Principal and assistant principal
- Grade-level or department leader
- Classroom teacher
- Counselor or intervention team

## User Stories

1. As an administrator, I want to compare grades and attendance by quarter so I
   can identify emerging school-wide risks.
2. As a grade-level leader, I want to compare trends by grade and subgroup so I
   can decide where deeper review is warranted.
3. As a teacher, I want to select one student and see academic, attendance,
   behavior, and intervention history in one place.
4. As an intervention-team member, I want to compare recorded outcomes by focus
   area while seeing sample size and methodological limitations.

## Functional Requirements

- Filter the overview by grade, race/ethnicity, gender, IEP, ELL, and
  performance level.
- Display average grade, attendance rate, incident count, and distinct students
  receiving an intervention.
- Show quarterly performance and behavior trends.
- Show the relationship between quarterly attendance and grade.
- Compare IEP and ELL quarterly averages with group sizes.
- Allow selection of one student for an integrated detail view.
- Preserve separate table grains to prevent many-to-many measure inflation.

## KPI Definitions

| KPI | Definition |
| --- | --- |
| Average Quarter Grade | Mean of `Quarter Grade` for records in filter context |
| Overall Attendance Rate | Total days present divided by total school days |
| Behavior Incidents | Sum of `Incident Count` |
| Students in Intervention | Distinct count of students with at least one intervention record |
| Positive Intervention Outcome | Outcome of Improving or Exited - Met Goal |

## Analytical Guardrails

- Describe associations without claiming causality.
- Always label the dataset as synthetic.
- Display or disclose small subgroup sizes.
- Do not use the dashboard to make automatic placement or disciplinary
  decisions.
- Require human review before acting on an attendance or performance flag.

## Acceptance Criteria

- Headline KPIs reconcile to source data: 80.28 average grade, 90.72% attendance,
  863 incidents, and 45 students with interventions.
- All quarter labels sort Q1 through Q4.
- Selecting a student updates every student-detail view consistently.
- Filters do not create duplicate or inflated measures.
- Dashboard labels remain legible at the published desktop size.
- The public project includes the data disclaimer and limitations.
