# Peakview Streaming subscriber data dictionary

**File:** `peakview_subscribers.csv` · **Rows:** 2,400 (one per subscriber) · **Columns:** 15

Peakview Streaming is a fictional video-streaming service. The data is synthetic and was created for IS 455. Peakview is the second business in every B worksheet, so the problems you solve for Canyon Fitness in each A worksheet come back here with new data.

The file is a snapshot of every active subscriber on **October 1, 2026**, plus what happened to each subscriber over the following 92 days (through January 1, 2027). Dates use the format `YYYY-MM-DD`. A blank cell means the event did not happen in that window.

| Column | Type | Description | Values |
| --- | --- | --- | --- |
| `subscriber_id` | Text | Unique subscriber ID | `S20000` to `S22399`; no duplicates |
| `signup_date` | Date | Date the subscriber signed up | Mar 3, 2020 to Aug 31, 2026 |
| `plan` | Text | Subscription plan | `Basic` (1,131), `Standard` (805), `Premium` (464) |
| `monthly_fee` | Decimal (US$) | Monthly price of the plan | Basic $8.99, Standard $14.99, Premium $22.99 |
| `region` | Text | Region of the billing address | `Mountain`, `Pacific`, `Midwest`, `South`, `Northeast` |
| `age` | Integer (years) | Account holder's age on October 1, 2026 | 18 to 75 |
| `hours_watched_last_30_days` | Decimal (hours) | Hours streamed in the 30 days before October 1, 2026, to the nearest half hour | 0 to 110 |
| `hours_watched_prior_30_days` | Decimal (hours) | Hours streamed in the 30 days before that (days 31–60 before October 1) | 0 to 125 |
| `days_since_last_login` | Integer (days) | Days from the subscriber's most recent login to October 1, 2026 | 0 (logged in on October 1) to 229; 30 or more whenever `hours_watched_last_30_days` is 0 |
| `autopay` | True/False | Whether the subscription is billed automatically | 75% `True` |
| `support_tickets_90_days` | Integer | Customer support tickets the subscriber opened in the 90 days before October 1, 2026 | 0 to 4 |
| `next_login_date` | Date | Date of the subscriber's first login after October 1, 2026 | Oct 2, 2026 to Jan 1, 2027; blank if no login in that window (306 subscribers) |
| `cancel_date` | Date | Date the subscriber cancelled | Oct 2 to Dec 31, 2026; blank if the subscriber did not cancel (224 cancelled) |
| `cancellation_reason` | Text | Reason the subscriber gave when cancelling | `Price`, `Not watching enough`, `Switched services`, `Finished a show`, `Billing problem`; blank if the subscriber did not cancel |
| `exit_survey_score` | Integer (1–5) | Satisfaction score from the survey sent at cancellation; 5 is most satisfied | 1 to 5; blank if the subscriber did not cancel |

## Notes

- A subscriber who cancelled has no logins after their cancellation date.
- There are no missing values except the blanks described above.
