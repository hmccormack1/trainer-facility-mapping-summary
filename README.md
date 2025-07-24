# Trainer-Facility Mapping (Summary): Workflow & Compensation Analysis

This case study summarizes an internal research and mapping project I conducted at StatStak to analyze how sports facilities manage their trainers and instructors. I reviewed meeting transcripts from dozens of client accounts to identify patterns in compensation models, access workflows, and platform configuration needs. The goal was to ensure that the product could support all edge cases and scale with flexibility.

## 🧠 Problem

StatStak’s clients use a variety of systems to manage instructors:
- Some pay hourly, others use revenue share or flat rates
- Some assign instructors manually, others let them self-schedule
- Reporting and payroll workflows vary widely

Without a clear taxonomy, it was hard to design universal platform logic.

## ⚙️ My Role

- Reviewed and analyzed onboarding transcripts account by account
- Identified and categorized:
  - Compensation structures (hourly, revenue %, etc.)
  - Instructor access workflows (manual vs. platform-based)
  - Reporting edge cases (overrides, multi-rate roles, etc.)
- Created a structured data model with 3 fields per account:
  - `trainer_comp_model`
  - `trainer_access_model`
  - `notes` (explanatory text)
- Flagged common pain points and proposed logic rules for platform automation

## 🔧 Tools Used

- Grain (transcript review platform)
- Structured tagging + categorization in spreadsheets
- Internal knowledge base contributions

## 🧪 Sample Output (Simplified)

```json
{
  "trainer_comp_model": "Hourly pay (e.g., $25/hr); set per instructor in user profile",
  "trainer_access_model": "Admin creates events from emailed schedules; instructors assigned to events",
  "notes": "Facility pays instructors hourly, configured per user profile. Admin can override rates per event if needed. Payroll reports auto-calculate based on duration × rate."
}
```

## 📈 Outcome

- Delivered a complete mapping of account models across the platform  
- Informed product decisions around payroll, scheduling, and permissions  
- Enabled scalable support for highly varied instructor workflows

## 🔒 Note

This is a summary of internal analysis work. No client names or sensitive data are included.
