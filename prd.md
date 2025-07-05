# Product Requirements Document (PRD): Livestack App

## Overview

Livestack is a mobile-first platform designed to help farmers and livestock managers track, monitor, and manage a variety of animals including turkeys, chickens, goats, and rams. The app enables users to record expenses, health data, feeding schedules, sales, and more while offering insights to improve animal welfare and profitability.

---

## Module 1: Onboarding & Authentication

### New User Registration

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Opens app and taps "Sign Up" | Loads registration form | Form is presented | Form loads within 2s |
| 2 | Inputs details: Name, Email, Phone, Farm Name | Validates fields | User proceeds | All fields validated |
| 3 | Taps "Continue" | Sends OTP to phone/email | OTP input screen shown | OTP received in ≤30s |
| 4 | Enters OTP | Verifies OTP | Redirects to onboarding | OTP must match |
| 5 | Accepts Terms & Policy | Stores acceptance | Navigates to dashboard | Consent stored |
| 6 | Registration complete | Sends welcome message | Access granted | Email/SMS received |

---

## Module 2: Livestock Management

### View All Livestock

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Opens "My Livestock" | Fetches records | Animals grouped by type | Data shown correctly |
| 2 | No animals yet | Shows empty state | Prompts to add animals | CTA visible |

### Add Livestock Group

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Taps “Add Group” | Opens form | User selects type and quantity | Form functional |
| 2 | Enters name, breed, quantity, cost | Saves data | New group added | Fields validated |
| 3 | Group added | Navigates to group dashboard | Ready to log activity | Entry persists |

### Record Daily Activity

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Selects group | Opens group dashboard | Shows options: feeding, health, expenses | Dashboard loads |
| 2 | Taps “Log Feeding” | Opens feeding form | User inputs feed type, quantity, cost | Form functional |
| 3 | Saves activity | Updates dashboard | Activity log updated | Data stored successfully |

---

## Module 3: Health & Expense Tracking

### Log Health Record

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Opens health tab | Loads health history | Empty or full history shown | Records displayed |
| 2 | Taps “Add Health Record” | Form appears | Inputs symptoms, treatment, vet cost | All inputs accepted |
| 3 | Saves entry | Entry saved to backend | Notification triggered | Health record stored |

### Track Expenses

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Taps “Expenses” tab | Loads expense categories | Feed, medication, housing, others | Tabs visible |
| 2 | Adds new expense | Form shows relevant fields | Inputs details | Form submits correctly |
| 3 | Saves expense | Dashboard updates | Financials adjusted | Expense visible in history |

---

## Module 4: Sales & Profit Calculation

### Record Sale

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Opens “Sales” tab | Shows sales history | List with buyer info and revenue | Sales records shown |
| 2 | Taps “Add Sale” | Opens sale form | Inputs animal group, quantity, price | Validation enforced |
| 3 | Saves sale | Updates group count and revenue | Group reduced | Sale reflected in logs |

---

## Module 5: Alerts & Reminders

### Set Reminder

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Opens “Reminders” | Sees existing reminders | Sorted by due date | Properly ordered |
| 2 | Taps “Add Reminder” | Selects category (feed, vaccine) | Sets date/time | Data saved |
| 3 | Reminder due | Sends notification | User alerted | Trigger within ±5 mins |

---

## Module 6: Reports & Insights

### View Reports

| Step | User Action | System Behavior | Expected Outcome | Acceptance Criteria |
|------|-------------|------------------|------------------|---------------------|
| 1 | Taps “Reports” | Loads financial & health stats | Weekly/monthly filters | Data is accurate |
| 2 | Filters by animal type | Updates charts | Visual graphs updated | Stats reflect data inputs |

---

## Notifications & Email Triggers

| Event | Type | Recipient | Purpose |
|-------|------|-----------|---------|
| Reminder Triggered | Push + Email | User | Alert for feeding, meds, sale |
| Expense Limit Exceeded | In-app | User | Budget alert |
| Sales Summary | Email | User | End-of-day report |
| Health Issue Recorded | Email | User | Summary of affected group |
| Group Mortality | Push | User | Warning & investigation prompt |

