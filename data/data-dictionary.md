# Data Dictionary

## `student_master.csv`

| Field | Type | Definition |
| --- | --- | --- |
| Student ID | Text | Fictional stable student key |
| First Name | Text | Fictional first name |
| Last Name | Text | Fictional last name |
| Grade | Integer | Grade level: 6, 7, or 8 |
| Gender | Text | Simulated gender category |
| Race/Ethnicity | Text | Simulated race or ethnicity category |
| IEP | Text | Simulated individualized education program indicator |
| ELL | Text | Simulated English language learner indicator |

## `test_scores.csv`

| Field | Type | Definition |
| --- | --- | --- |
| Student ID | Text | Student key |
| Quarter | Text | Academic quarter Q1-Q4 |
| Period | Text | Quarter and simulated year label |
| Unit Test Score | Decimal | Quarterly unit-test score |
| Vocabulary Quiz Score | Decimal | Quarterly vocabulary score |
| Lab Performance Score | Decimal | Quarterly lab score |
| Quarter Grade | Decimal | Simulated overall quarterly grade |
| Performance Level | Text | Advanced, Proficient, Developing, or Below Basic |

## `attendance.csv`

| Field | Type | Definition |
| --- | --- | --- |
| Student ID | Text | Student key |
| Quarter | Text | Academic quarter Q1-Q4 |
| Period | Text | Quarter and simulated year label |
| Total School Days | Integer | Available instructional days |
| Days Present | Integer | Days recorded present |
| Days Absent | Integer | Days recorded absent |
| Days Tardy | Integer | Days recorded tardy |
| Attendance Rate (%) | Decimal | Days present divided by total school days, expressed as a percentage |
| Chronic Absentee (>10%) | Text | Yes when absences exceed 10% of available days |

## `behavior_incidents.csv`

| Field | Type | Definition |
| --- | --- | --- |
| Student ID | Text | Student key |
| Quarter | Text | Academic quarter Q1-Q4 |
| Period | Text | Quarter and simulated year label |
| Incident Type | Text | Simulated behavior category |
| Action Taken | Text | Simulated response |
| Incident Count | Integer | Number of incidents represented by the row |

Quality note: the file contains 40 exact duplicate rows. Because it lacks an
incident ID and event date, identical records cannot be distinguished from
legitimate repeated events. The dashboard treats `Incident Count` as the
measure; a production system should add a unique incident key and event date.

## `interventions.csv`

| Field | Type | Definition |
| --- | --- | --- |
| Student ID | Text | Student key |
| Quarter Started | Text | Quarter in which the intervention began |
| Period | Text | Quarter and simulated year label |
| Intervention Type | Text | Named intervention |
| Focus Area | Text | Academic, Attendance, Behavioral, or Social-Emotional |
| Status | Text | Current state of the intervention |
| Outcome | Text | Improving, Stable, No Change, or Exited - Met Goal |

Quality note: outcome labels are descriptive and do not establish that an
intervention caused the observed outcome.
