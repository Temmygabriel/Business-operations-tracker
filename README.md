# 📊 Acetrue Technologies — Business Operations & Inventory Tracker

> A two-file Excel system for managing daily operations, inventory, sales, expenses and profit & loss for a small electronics retail business.

---

## 🗂️ The Two-File System

This project uses two separate Excel files designed for different users:

| File | Who It's For | What It Contains |
|------|-------------|-----------------|
| `Acetrue_Technologies_Tracker.xlsx` | Business Owner | Full system — inventory, sales, stock in, expenses, P&L, dashboard |
| `Acetrue_SalesStaff_Log.xlsx` | Sales Staff | Sales log + expenses only — simplified for daily data entry |

The two files are designed to work together. The sales staff logs transactions daily in their file. At the end of each day or week, the owner copies those entries into the master tracker, which then auto-updates the dashboard, inventory levels, and P&L.

---

## 📁 Master Tracker — Sheet Breakdown

### 📊 DASHBOARD
The owner's command centre. Opens every morning to show:
- Today's revenue, items sold, and total inventory value (KPI cards)
- Live low-stock alerts with red/yellow/green status for all 13 products
- Month-to-date revenue breakdown by product

### 📦 INVENTORY
Master stock list. Tracks:
- Opening stock, stock received, stock sold, damaged/adjustments
- Current stock (auto-calculated)
- Cost price, selling price, total stock value
- Reorder level alerts with conditional formatting

### 💰 DAILY SALES
Sales transaction log. Features:
- Product dropdown (data validation)
- Unit price auto-fills from inventory
- Total auto-calculates from qty × price
- Payment method tracking (Cash / POS / Transfer)
- End-of-day summary panel

### 📥 STOCK IN
Purchase and restock log. Records:
- Date, product, quantity received, unit cost
- Total purchase cost (auto-calculated)
- Supplier name and invoice/receipt number

### 💸 EXPENSES
Business expense log. Includes:
- Categorised expenses (Rent, Salary, Transport, Data, Packaging, etc.)
- Payment method tracking
- Monthly and all-time totals

### 📈 PROFIT & LOSS
Auto-calculated summary showing:
- Total revenue, COGS, gross profit, gross margin %
- Total operating expenses
- Net profit and net margin %

---

## 📁 Staff Log — Sheet Breakdown

### 💰 DAILY SALES
Simplified sales entry with:
- Product dropdown (same 13 products)
- Price auto-fills — staff cannot enter wrong price
- Total auto-calculates
- End-of-day revenue and payment-method totals

### 💸 DAILY EXPENSES
Simple expense entry with:
- Category dropdown
- Daily and monthly totals auto-calculated

### 📋 QUICK GUIDE
Plain-English instructions written for non-technical staff. Opens by default when the file is launched.

---

## 🔄 How the Two Files Work Together

### Daily Workflow

```
Morning:       Owner checks 📊 DASHBOARD — reviews stock alerts
During day:    Sales staff logs every sale in Acetrue_SalesStaff_Log.xlsx
End of day:    Owner copies staff entries into master tracker (5 mins)
               Owner logs any business expenses
Weekly:        Owner reviews 📈 PROFIT & LOSS
```

### How to Copy Staff Entries into the Master File

1. Open **both** files side by side (View → Arrange All → Vertical in Excel)
2. In the Staff Log, go to **💰 DAILY SALES**
3. Select all new rows entered today (click the row number on the left, drag to select multiple rows)
4. Right-click → **Copy**
5. Switch to the Master Tracker → **💰 DAILY SALES** sheet
6. Click the first empty row in column B (Date column)
7. Right-click → **Paste Special** → **Values Only** (this is important — paste values, not formulas)
8. The Dashboard and Inventory will update automatically
9. Repeat the same process for **💸 EXPENSES**

> ⚠️ Always use **Paste Special → Values Only** when copying between files. This prevents formula reference errors.

---

## ⚙️ First-Time Setup

1. Open `Acetrue_Technologies_Tracker.xlsx`
2. Go to **📦 INVENTORY**
3. Update **Opening Stock** (column C) with current stock counts
4. Update **Cost Price** (column I) and **Selling Price** (column J) with your real prices
5. Update **Reorder Level** (column H) — the minimum qty before you restock
6. Save the file — everything else auto-calculates from here

---

## 🛠️ Excel Skills Demonstrated

| Skill | Where Used |
|-------|-----------|
| `SUMIF` | Inventory stock sold, daily revenue totals |
| `SUMPRODUCT` | Monthly revenue, payment-method breakdowns |
| `VLOOKUP` | Auto-fill unit price from product name |
| `IFERROR` | Prevent divide-by-zero and blank cell errors |
| `IF` / Nested `IF` | Status flags, conditional calculations |
| `TEXT`, `MONTH`, `YEAR`, `TODAY` | Date-based filtering and display |
| Data Validation | Dropdown lists for products, payment methods, categories |
| Conditional Formatting | Low stock red/yellow/green alerts |
| Cross-sheet referencing | Live links between all sheets |
| Named ranges & absolute references | Formula integrity across 500-row tables |

---

## 📦 Products Tracked

EarPods · Button Phone · Memory Card · Charger · Tripod Stand · Selfie Stick · Cables · Ringlight · Speakers · Wireless Mic · Mouse · Powerbanks · Smartwatch

---

## 👤 Author

Built by TemmyGabriel as a portfolio project demonstrating Excel-based business intelligence and operations system design.


