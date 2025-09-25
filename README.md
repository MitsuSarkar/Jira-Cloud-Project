# Jira Finance Variance Dashboard

This project shows how I adapted **Jira Cloud** (typically used by software teams) to run a **finance variance review workflow** for month-end close.

## What’s inside
- `/data` — CSV/JSON exports from Jira (issues, overdue items, open items).
- `/docs` — Screenshots of the Jira Dashboard and automation rules.
- `README.md` — Process, setup, and how to reproduce.

## Workflow (high level)
1. **Data intake** via CSV (Budget vs Actuals: Variance Amount, Variance %, Cost Center, Period).
2. **Custom fields** in Jira: Cost Center, Variance %, GL Account, Period (month), Due date.
3. **Automation rules**
   - Flag material variances (e.g., Variance % > 10) → set Priority = High + move to Ready for Review.
   - Month-end reminder (scheduled) → comment on issues due this month.
4. **Saved filters**
   - All Open Items
   - Overdue Variances
   - Due within next 30 days
   - Variance % > 10
5. **Dashboard gadgets**
   - Pie by Cost Center
   - Filter Results (Overdue)
   - Two-Dimensional (Status × Assignee)
   - Created vs Resolved
   - Average Age
<img width="1912" height="894" alt="jira dashboard 1" src="https://github.com/user-attachments/assets/730d2b75-2da1-400e-9217-dd2a169be440" />
<img width="1587" height="860" alt="jira dashboard 2" src="https://github.com/user-attachments/assets/d6169d44-efb6-4afe-bccd-035a42ec13e0" />


## How to reproduce (Jira Cloud)
- Create a project (Team-managed or Company-managed).
- Add custom fields: Cost Center (select), Variance Amount (%/number), Period (date).
- Import CSV or create a few issues manually.
- Recreate saved filters (see `/data` for examples/columns).
- Build the dashboard with the gadgets listed above.

## Notes
- Data here is sample/demo data exported from my Jira Cloud sandbox.
- Screenshots are for demonstration — no confidential info.

