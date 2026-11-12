# Canyon Fitness member data: data dictionary

**File:** `canyon_fitness_members.csv` · **Rows:** 2,000 (one per member) · **Columns:** 15

Canyon Fitness is a fictional chain of gyms in Provo, Orem, Lehi and Sandy, Utah. The data is synthetic and was created for IS 455.

The file is a snapshot of every active member on **October 1, 2026**, plus what happened to each member over the following 92 days (through January 1, 2027). Dates use the format `YYYY-MM-DD`. A blank cell means the event did not happen in that window.

| Column | Type | Description | Values |
| --- | --- | --- | --- |
| `member_id` | Text | Unique member ID | `M10000` to `M11999`; no duplicates |
| `join_date` | Date | Date the member joined | Oct 28, 2021 to Sep 1, 2026 |
| `plan` | Text | Membership plan | `Basic` (1,095), `Plus` (609), `Family` (296) |
| `monthly_fee` | Integer (US$) | Monthly price of the plan | Basic $29, Plus $45, Family $79 |
| `home_gym` | Text | Location where the member is registered | `Provo`, `Orem`, `Lehi`, `Sandy` |
| `age` | Integer (years) | Member's age on October 1, 2026 | 16 to 73 |
| `visits_last_30_days` | Integer | Check-ins in the 30 days before October 1, 2026 | 0 to 38; can exceed 30 because some members check in twice a day |
| `visits_prior_30_days` | Integer | Check-ins in the 30 days before that (days 31–60 before October 1) | 0 to 45 |
| `days_since_last_visit` | Integer (days) | Days from the member's most recent check-in to October 1, 2026 | 0 (visited on October 1) to 197; 30 or more whenever `visits_last_30_days` is 0 |
| `autopay` | True/False | Whether the membership is billed automatically | 70% `True` |
| `support_tickets_90_days` | Integer | Customer support tickets the member opened in the 90 days before October 1, 2026 | 0 to 4 |
| `next_visit_date` | Date | Date of the member's first check-in after October 1, 2026 | Oct 2, 2026 to Jan 1, 2027; blank if no check-in in that window (266 members) |
| `cancel_date` | Date | Date the member cancelled | Oct 2 to Dec 31, 2026; blank if the member did not cancel (124 cancelled) |
| `cancellation_reason` | Text | Reason the member gave when cancelling | `Cost`, `Not using it`, `Joined another gym`, `Moving`, `Injury`; blank if the member did not cancel |
| `exit_survey_score` | Integer (1–5) | Satisfaction score from the survey sent at cancellation; 5 is most satisfied | 1 to 5; blank if the member did not cancel |

## Notes

- A member who cancelled has no check-ins after their cancellation date.
- There are no missing values except the blanks described above.
