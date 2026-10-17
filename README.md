# 🏦 Banking Analytics Dashboard: Customer & Money Performance


---

## 📖 Project Overview

This project is an easy-to-use **Banking Dashboard** built with Microsoft Power BI. It helps bank managers quickly see how customers use their accounts, how money moves in and out of the bank, and who is taking out loans.

The project looks at bank records for the entire year of 2025:

- **1,000 customers** in total
- **$54M** sitting in customer bank accounts
- **$52M** moved through deposits, withdrawals, and transfers
- **$359M** given out in loans

The goal was to turn raw data into a clear, clean screen that bank leaders can look at to make smart business choices.

---

## 🎯 Project Goals

- Bring raw bank data into Power BI and clean it up.
- Fix mistakes, fill in blanks, and make sure numbers and dates are set correctly.
- Write simple formulas (DAX) to calculate key totals like customer counts, account balances, and average credit scores.
- Redesign the dashboard with bright, clear colors and neat cards so it is easy to read.
- Find helpful patterns in the data to help the bank grow and serve customers better.

---

## 📂 The Data Used

The dataset covers bank activities from **January 1, 2025, to December 31, 2025**.

| Category | Fields Included |
|---|---|
| **Customer Info** | Customer ID, Age, Gender, City, Region |
| **Account Type** | Savings, Current, Salary |
| **Transactions** | Date, Type (Deposit, Withdrawal, Transfer, Payment), Channel (Mobile App, Online, ATM, Branch), Amount |
| **Loans & Balances** | Account Balance, Loan Status (Approved, Pending, Rejected, No Loan), Loan Amount, Credit Score |

---

## 🛠 Tools Used

- 📊 **Microsoft Power BI:** To build the charts, cards, and interactive dashboard.
- 🔄 **Power Query:** To clean up messy data, fix columns, and remove errors.
- 📈 **DAX (Data Analysis Expressions):** To write the formulas for the dashboard numbers.
- 📂 **Microsoft Excel / CSV:** Where the raw data was stored.

---

## 🧹 Data Cleaning & Preparation

Before building charts, the raw data was cleaned in Power Query using these steps:

1. **Loaded the Data:** Brought the raw bank file into Power BI.
2. **Fixed Column Types:** Made sure customer IDs were recognized as text, dates as calendar dates, and amounts as currency values.
3. **Handled Empty Spots:** Customers who never applied for a loan were labeled clearly as `"No Loan"` so they wouldn't be counted as missing data.
4. **Cleaned Text:** Removed accidental spaces and made sure city and channel names were spelled consistently.
5. **Grouped Dates:** Split transaction dates into months and quarters (`Qtr 1` to `Qtr 4`) to see how business changes throughout the year.
6. **Created Calculations (DAX):** Wrote simple formulas to add up the main dashboard numbers.

### Key Formulas Used

**Count Total Customers**

```dax
Total Customers = DISTINCTCOUNT('Banking_Data'[Customer ID])
```

**Add Up All Account Balances**

```dax
Total Account Balance = SUM('Banking_Data'[Account Balance])
```

**Add Up Total Money Moved**

```dax
Total Transaction Amount = SUM('Banking_Data'[Transaction Amount])
```

**Add Up All Loans**

```dax
Total Loan Amount = SUM('Banking_Data'[Loan Amount])
```

**Calculate Average Credit Score**

```dax
Average Credit Score = AVERAGE('Banking_Data'[Credit Score])
```

**Count Customers Without Loans**

```dax
Customer No Loan =
CALCULATE(
    DISTINCTCOUNT('Banking_Data'[Customer ID]),
    FILTER(
        'Banking_Data',
        'Banking_Data'[Loan Status] = "No Loan"
    )
)
```

---

## 📊 Dashboard Walkthrough

### Key Numbers at the Top (KPIs)

- 👥 **Total Customers:** 1,000 people bank here.
- 💰 **Total Account Balance:** $54M is saved in accounts.
- 💳 **Total Transaction Amount:** $52M was moved during the year.
- 📄 **Total Loan Amount:** $359M has been loaned out.
- 🎯 **Average Credit Score:** 702.01 (a good, healthy score).
- 🚫 **Customers Without a Loan:** 547 people do not have a loan.

### Charts on the Screen

- **Monthly Activity (Wave Chart):** Shows how much money moved each month. Business peaks in the middle of the year (July and August).
- **Types of Transactions (Bar Chart):** Shows where money went. Deposits ($15.6M) were higher than withdrawals ($13.3M) and transfers ($13.1M).
- **Customers by Region & City (Bar Charts):** Shows where customers live. Most are in the West (401) and South (358), especially in cities like Mumbai and Ahmedabad.
- **How Customers Bank (Bar Chart):** Shows how people access their money. Mobile app (333) and online banking (327) are used far more than physical branches (149).
- **Account Types (Donut Chart):** About 60% of people have Savings accounts, 21% have Current accounts, and 19% have Salary accounts.
- **Loan Applications (Colored Bar Chart):** Approved loans are green (258), rejected are red (98), pending are yellow (97), and customers with no loan are dark blue (547).
- **Filters on the Left:** Quick buttons to filter the whole page by Quarter, Region, Gender, or Channel.

---

## 📈 Simple Insights (What the Data Tells Us)

1. **People Prefer Phones Over Branches:** Two out of every three customers bank on their phone or computer, while very few visit a physical branch.
2. **More Money Comes In Than Goes Out:** Deposits ($15.6M) are higher than withdrawals ($13.3M), showing that customer savings are stable.
3. **Summer Is the Busiest Time:** Money movement jumps in July ($5.4M) and August ($5.1M) compared to the rest of the year.
4. **Huge Opportunity for Loans:** More than half the customers (547) have never taken a loan, and their credit scores are solid (average 702), making them good candidates for future loans.

---

## 💡 Recommendations (What the Bank Should Do)

1. **Offer Loans to Reliable Savers:** Reach out to the 547 customers without loans and offer them credit cards or small loans, since their credit scores are already good.
2. **Invest in Mobile Apps, Not More Branches:** Since most customers bank digitally, put more money into keeping the app fast and simple rather than opening new physical branches.
3. **Prepare for Summer Spikes:** Make sure banking systems and cash reserves are ready for July and August, when transaction volume is highest.
4. **Speed Up Pending Loans:** Make quick decisions on the 97 pending loan applications so customers don't get frustrated and look at other banks.

---

## 📚 Skills Used in This Project

- Cleaning messy data
- Changing data types and handling blank values
- Writing DAX formulas for sums, averages, and counts
- Designing clean, easy-to-read charts
- Choosing colors that highlight important data
- Turning data into simple business advice

---

## 📌 Conclusion

This project shows how raw banking data can be transformed into an easy, visual tool. With this dashboard, managers can quickly understand their customers, spot trends, and make smart decisions to grow the bank's business safely.

---

## 👩‍💻 Developed By

**Esther Jimbo**
Power BI Data Analyst



