# ✈️ Aircraft Maintenance Summary Tracker

A portfolio project that simulates a real-world SQL workflow to generate an aircraft maintenance summary report. This query consolidates historical maintenance data and forecasted events into a single output—ideal for dashboards, planning tools, and compliance tracking.

---

## 📌 Project Objective

To produce a clean, summarized maintenance dataset per aircraft by combining past events (like C-checks or lighter checks) and future forecast data (like weight and balance checks). The goal is to support operational decision-making in fleet maintenance management.

---

## 🗂️ Data Sources (Simulated)

This query is based on fictional or sanitized versions of the following tables:

| Table Name        | Description                                         |
|-------------------|-----------------------------------------------------|
| `aircrafts`       | Contains aircraft type, delivery info, and status   |
| `work_orders`     | Historical maintenance events per aircraft          |
| `maintenance_logs`| Logged checks with timestamps, flight hours, cycles|
| `forecast_data`   | Future-dated checks (calendar-based and operational)|

> ⚠️ All data has been anonymized or simulated to protect confidentiality. This is a recreation of a real business use case that I worked on using fake data.

---

## 🧠 Key Features

- ✅ Joins multiple maintenance sources (logs, work orders, and forecasts)
- 🧮 Uses conditional logic to handle static vs. dynamic check data
- 🗓️ Applies `DATEADD` and custom epoch handling to convert offsets into readable dates
- 🕒 Formats flight hours from raw values into `HH:MM` style
- 🚫 Filters out retired or irrelevant aircraft

---

## 🔍 Example Use Cases

- Maintenance planning dashboards
- Aircraft compliance and lifecycle tracking
- Visual reporting tools (e.g., Power BI, Tableau)

---

## ⚙️ Techniques Used

- SQL joins and subqueries
- `CASE WHEN` logic for fallback values
- Windowed aggregates (`MAX`, `MIN`)
- Date math and formatting with `DATEADD`, `CAST`, and `CONVERT`
- Clean aliasing and consistent formatting for readability

---

## 🧪 Sample Output

Here’s a fictional preview of what the output might look like:

| aircraft_id | aircraft_type | delivery_date | last_c_check_date | next_heavy_maintenance | next_calendar_check_date |
|-------------|----------------|----------------|--------------------|------------------------|---------------------------|
| A001        | TYPE_X         | 2015-03-15     | 2022-11-02         | 2025-07-15             | 2025-03-01                |
| A002        | TYPE_Y         | 2016-08-20     | 2023-05-28         | 2026-01-10             | 2025-12-01                |

---

## 📊 Bonus: Dashboard (Optional)

You can visualize this query in tools like:

- Power BI (for scheduling views)
- Tableau (to map maintenance over time)
- Excel (for static reporting)

> I’ve included a `dashboard_mock.png` and `sample_output.csv` in this repo for demo purposes.

---

## 🛠️ Tools Used

- SQL Server (T-SQL)
- GitHub for version control
- (Optional) Power BI / Tableau for visualization

---

## 🗒️ Notes

This project is inspired by a real-world aircraft maintenance analysis I performed professionally.  
All sensitive data, table names, and business logic have been abstracted or recreated with dummy datasets to respect confidentiality.

---

## 🙌 Want to Collaborate?

Feel free to fork this repo, open an issue, or reach out via [LinkedIn](#) if you'd like to collaborate on SQL or data analytics projects.
