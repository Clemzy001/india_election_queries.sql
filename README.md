# 🗳️ India General Elections 2024 - SQL Data Analysis

## 📊 Project Overview
This project involves analyzing **India's 2024 General Election** data using **SQL** to derive insights about political party performances, alliances, vote distributions, and constituency-level dynamics. The dataset includes details from multiple tables such as state-wise results, party performance, and voting breakdowns (EVM & postal).

---

## 🧰 Tools & Technologies Used
- **SQL Server / PostgreSQL / MySQL** (compatible with most)
- **SQL Joins, CTEs, Aggregates, Window Functions**
- **DBMS**: SQL Management Studio / DBeaver / pgAdmin (based on your setup)

---

## 📁 Datasets / Tables Involved
- `constituencywise_details` – Candidate-level vote details
- `constituencywise_results` – Winning candidate and margin
- `partywise_results` – Party-wise seat wins
- `statewise_results` – Mapping of constituencies to states
- `states` – List of all states with metadata

---

## 🧩 Key Questions Answered

### 🪑 Total Seats & Alliances
- ✅ Total number of seats in 2024 elections
- ✅ Seats won by **NDA**
- ✅ Seats won by **I.N.D.I.A**
- ✅ Seats won by **OTHER** parties

### 🏆 Party & Alliance Analysis
- Top winning parties in a specific state (e.g. Andhra Pradesh)
- Seat distribution by party alliance in each state
- Seat count breakdown by alliance using dynamic updates via `ALTER TABLE` & `UPDATE`

### 🧠 Constituency-Level Insights
- Winner, party, total votes, and margin for specific constituencies
- Highest EVM votes per constituency
- EVM vs postal vote analysis per candidate
- Winner vs runner-up in every constituency of a specific state (e.g. Maharashtra)

---

## 🧪 Highlights of SQL Features Used
- **`GROUP BY` + `SUM`**: for aggregating seat counts
- **`CASE WHEN`**: for conditional logic (alliances)
- **`JOIN` operations**: to connect multiple tables
- **`CTE (WITH)`** + **`ROW_NUMBER()`**: to rank candidates and find runner-ups
- **`ALTER TABLE` + `UPDATE`**: to add party alliance dynamically

---

## 🚀 How to Use
1. Clone this repository.
2. Import the dataset into your SQL database (ensure correct schema/table structure).
3. Run the `.sql` file queries in your SQL environment (e.g. SSMS, DBeaver, pgAdmin).
4. Modify `WHERE` clauses as needed for custom state/constituency insights.

---

## 📊 Sample Queries
### Total Seats:
```sql
SELECT COUNT(DISTINCT Parliament_Constituency) AS Total_Seats
FROM constituencywise_results;
