# Practice Case Study: Bank Feed Reconciliation & P&L Review
### Sample Company: Craig's Design and Landscaping Services (QuickBooks Online Test Drive)

---

## Overview

This exercise focused on clearing a full bank feed queue across three accounts (Checking, Savings, and Mastercard) inside QuickBooks Online — matching, categorizing, and posting transactions — followed by a review of the resulting Profit & Loss report. Along the way, two data-quality issues surfaced that are worth flagging from a professional bookkeeping standpoint, plus one deeper investigation into a misleading P&L line item.

**Skills demonstrated:**
- Bank feed transaction matching and categorization
- Vendor and customer creation on the fly
- Reading and interpreting a Profit & Loss report
- Root-cause investigation of an unusual account balance
- Professional judgment on when to escalate to a client rather than assume

---

## Part 1: Clearing the Bank Feed Queues

### Starting Point
The dashboard showed three accounts with pending bank feed items:

| Account | Bank Balance | Pending Items |
|---|---|---|
| Checking | -$3,621.93 | 25 |
| Savings | $200.00 | 1 |
| Mastercard | $304.96 | 7 |

### Checking Account (25 → 0)
Worked through the queue matching suggested transactions (e.g., Hicks Hardware, PG&E, customer deposits) and creating new vendors/customers where none existed yet (e.g., "Books by Bessie" for a landscaping income deposit).

Midway through, QuickBooks flagged a **duplicate/error warning**: three "A Rental" transactions appeared in the queue, two of them showing error icons on their categorization. A separate line item, "Squeaky Kleen Car," also showed **"2 matches found,"** requiring manual review instead of an automatic match.

After resolving the vendor assignments and posting the remaining categorized items, the Checking queue cleared completely — **Posted balance moved from $1,201.00 to -$568.38**, reflecting the newly recorded transactions.

### Savings Account (1 → 0)
A single $200.00 deposit matched cleanly to an existing entry — no complications.

### Mastercard Account (7 → 0)
Similar pattern to Checking: several transactions needed new vendors (Amazon, Lara's Lamination), while others had system-suggested matches. Two separate "Squeaky Kleen Car" charges ($19.99 each, dated 07/13 and 07/20) both showed "2 matches found" — flagged as a possible duplicate posting rather than accepted at face value.

**Result:** All 33 original pending transactions across the three accounts were matched, categorized, and posted — Checking, Savings, and Mastercard all reached "all caught up" status.

---

## Part 2: Professional Judgment Notes

Two issues came up during the exercise that, in a real client engagement, should never be resolved by guessing:

**1. Vendor naming ambiguity — "A Rental" vs. "A1 Rental"**
QuickBooks auto-suggested "A1 Rental" as the vendor for transactions where the bank feed description read "A Rental." For the purposes of completing this practice exercise, the system suggestion was accepted. In a live engagement, this should be treated differently: a bookkeeper should never assume a vendor's correct identity from a software suggestion alone. The correct step is to pause and confirm the accurate name with the client — accepting an unverified guess risks creating a duplicate vendor record and fragmenting that vendor's expense history across two names.

**2. Landscaping income categorization**
Category suggestions for landscaping-related income were followed as presented during the walkthrough, again for the sake of completing the exercise. In practice, income categorization should be verified against the client's actual chart of accounts and how they define their revenue streams, not accepted from a generic system suggestion.

**Takeaway:** Software suggestions are a starting point, not a substitute for verification. When data is ambiguous, the professional response is to flag it and ask — not to guess.

---

## Part 3: Investigating a Misleading P&L Line

After clearing the bank feeds, the Profit & Loss report (Jan 1 – Aug 3, 2026) showed:

- **Total Income:** $10,200.77
- **Net Operating Income:** $2,674.07
- **Net Income (bottom line):** **-$241.93**

That $2,916 swing between a healthy operating result and a negative bottom line traced back to a **Miscellaneous Expense** line sitting under "Other Expenses."

**Root cause:** Three opening balance entries had been posted using **Bills** rather than a direct journal entry against an equity account. Because a Bill always posts its debit side to an expense account, QuickBooks routed these non-operational setup entries into Miscellaneous Expense instead of Opening Balance Equity. Since Miscellaneous sits below the operating line, it didn't distort Net *Operating* Income — but it still dragged the final Net Income into negative territory.

**Why this matters:**
1. **Skews profitability at a glance** — a reader checking only the bottom line would wrongly conclude the business lost money, when operations were actually profitable.
2. **Tax implications** — operating expenses and equity adjustments are treated differently for tax purposes; misclassifying one as the other creates confusion at tax time.
3. **Misleads external stakeholders** — banks, investors, or buyers reviewing a standard P&L rarely drill into sub-line detail. A negative Net Income on the face of the report can misrepresent the company's real financial health.

**Correct fix:** Reclassify the opening balance entries out of Miscellaneous Expense and into Opening Balance Equity (or Retained Earnings) via journal entry. As a preventive measure, many bookkeepers also restrict or rename default "Miscellaneous"/"Uncategorized" accounts in the Chart of Accounts so setup entries can't accidentally land there again.

---

## Key Takeaways

- Cleared 33 bank feed transactions across 3 accounts from scratch, including vendor/customer creation and error resolution
- Identified and flagged a vendor-naming inconsistency and a possible duplicate transaction rather than accepting system suggestions blindly
- Diagnosed the root cause of a misleading Net Income figure and identified the correct accounting fix
- Reinforced a core principle of professional bookkeeping: **when in doubt, clarify with the client — don't guess**
