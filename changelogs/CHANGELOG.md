## Version 1.2.3 — July 9, 2026

### What's New
* Fixed an issue where total attendance hours could be calculated incorrectly.
* **New Feature: Staff info-Board Summary** (beta)
* Improved overall stability and performance.


## Version 1.2.2 — July 7, 2026
### What's New
* Enhanced Leave History.
* Enhanced Leave Overview.
* Enhanced Attendance History.
* Enhanced My Timesheet Entries
* Enhanced Staff Activity
* Updated **Lights Out** to allow users to clock out without requiring a minimum of 8 recorded work hours.
* Separated **Lights Out** from daily timesheet validation, allowing timesheets to be completed within the 3-day grace period.
* **New Feature: Customize Action Cards** – Personalize your action cards by going to **Appearance → Action Card Style → See All → Customize**. Create your own card designs, share them with others, or import custom styles by scanning a shared QR code.
* General bug fixes, performance improvements, and stability enhancements.

#### Timesheet Lock/Unlock Behavior (Consistent Across All Scenarios)

You can make the expected action consistent across all lock scenarios:

---

##### **Scenario 1 – No Lock**

**Current Day:** 10 Jul

| Date  |    Hours | Status                  |
| ----- | -------: | ----------------------- |
| 9 Jul | 7h (<8h) | Within amendable period |
| 8 Jul | 5h (<8h) | Within amendable period |
| 7 Jul | 6h (<8h) | Within amendable period |

**Amendable Days:** 9 Jul, 8 Jul, 7 Jul
**Result:** **No Lock**

**User Action:**
* User can create, update, or delete timesheet entries for **9 Jul, 8 Jul, and 7 Jul**.
* **No unlock request is required.**

---

##### **Scenario 2 – Lock**

**Current Day:** 10 Jul

| Date  |    Hours | Status                   |
| ----- | -------: | ------------------------ |
| 9 Jul | 7h (<8h) | Within amendable period  |
| 8 Jul | 5h (<8h) | Within amendable period  |
| 7 Jul | 6h (<8h) | Within amendable period  |
| 6 Jul | 3h (<8h) | Outside amendable period |

**Amendable Days:** 9 Jul, 8 Jul, 7 Jul
**Result:** **Lock**
**Reason:** 6 Jul is outside the 3-day amendable period and has fewer than 8 recorded hours.

**User Action:**
* User **must submit a Timesheet Unlock Request** before any timesheet entries can be amended.

---

##### **Scenario 3 – Lock**

**Current Day:** 10 Jul

| Date  |    Hours | Status                   |
| ----- | -------: | ------------------------ |
| 9 Jul | 7h (<8h) | Within amendable period  |
| 8 Jul | 5h (<8h) | Within amendable period  |
| 7 Jul | 6h (<8h) | Within amendable period  |
| 6 Jul | 3h (<8h) | Outside amendable period |
| 3 Jul | 0h (<8h) | Outside amendable period |

**Amendable Days:** 9 Jul, 8 Jul, 7 Jul
**Result:** **Lock**
**Reason:** Incomplete timesheets exist outside the amendable period (6 Jul and 3 Jul).

**User Action:**
* User **must submit a Timesheet Unlock Request** before any timesheet entries can be amended.

---

##### **Scenario 4 – Lock**

**Current Day:** 10 Jul

| Date  |      Hours | Status                   |
| ----- | ---------: | ------------------------ |
| 9 Jul |   7h (<8h) | Within amendable period  |
| 8 Jul |   5h (<8h) | Within amendable period  |
| 7 Jul |   6h (<8h) | Within amendable period  |
| 6 Jul |   3h (<8h) | Outside amendable period |
| 3 Jul |   0h (<8h) | Outside amendable period |
| 2 Jul | 2.5h (<8h) | Outside amendable period |
| ...   |        ... | Outside amendable period |

**Amendable Days:** 9 Jul, 8 Jul, 7 Jul
**Result:** **Lock**
**Reason:** One or more incomplete timesheets exist outside the amendable period (e.g., 6 Jul, 3 Jul, 2 Jul, ...).

**User Action:**
* User **must submit a Timesheet Unlock Request** before any timesheet entries can be amended.

---

##### **Rule Summary**
* **Amendable Period:** The latest **3 days**, excluding the current day.
* Users may freely create, update, or delete timesheet entries within the amendable period.
* If **any date older than the amendable period** has **less than 8 recorded hours**, the timesheet is **locked**.
* **When locked, users must submit a Timesheet Unlock Request before any timesheet entries can be amended.**

## Version 1.2.1 — July 2, 2026

### What's New

- Introduced eApproval
- Enhanced overall app performance and reliability
- General improvements and bug fixes

---

## Version 1.2.0 — June 25, 2026

### What's New

- Improved timesheet log selection
- Improved Canvas approval experience
- Added required remarks when submitting unlock requests
- Improved app update checking to help ensure you stay on the latest version
- Enhanced overall app performance and reliability
- General improvements and bug fixes

---

## Version 1.1.9 — June 18, 2026

### What's New

- Enhanced login experience and clearer messages
- Added support for creating timesheets exceeding 12 total hours with feedback prompts
- Improved Customer No. selection experience
- Improved app performance and reliability
- General improvements and bug fixes
  
---

## Version 1.1.8 — June 16, 2026 (**BETA Release**)


