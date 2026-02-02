# De-zoomcamp-module-2
Module 2 of the zoomcamp homework

This repository contains my solution for **Homework 2: Workflow Orchestration** in the **Data Engineering Zoomcamp 2026**.

The goal of this homework is to extend the existing Kestra workflows to process **NYC Taxi data for the year 2021** (January–July) for both **Yellow** and **Green** taxi datasets, and to answer quiz questions based on the workflow executions.

---

## 📂 Repository Structure

```
.
├── flows/
│   ├── yellow_taxi_flow.yml
│   ├── green_taxi_flow.yml
│   └── backfill_2021.yml
├── README.md
```

---

## 🧠 Homework Tasks

* Extended existing Kestra flows to include **2021 data (Jan–Jul)**
* Processed **both Yellow and Green taxi datasets**
* Used **Kestra backfill functionality** to load historical data
* Verified outputs (file sizes, row counts)
* Answered quiz questions based on execution results

---

## 🚕 Dataset

NYC TLC Trip Record Data (Green & Yellow taxis)

Source:

* [https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/green](https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/green)
* [https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/yellow](https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/yellow)

Download pattern used in flows:

```
https://github.com/DataTalksClub/nyc-tlc-data/releases/download/{taxi}/{taxi}_tripdata_{year}-{month}.csv.gz
```

---

## 📊 Quiz Answers

**Q1. Uncompressed file size for Yellow Taxi – December 2020**
✅ 134.5 MiB

**Q2. Rendered value of `file` variable (green, 2020, 04)**
✅ `green_tripdata_2020-04.csv`

**Q3. Total rows for Yellow Taxi data in 2020**
✅ 24,648,499

**Q4. Total rows for Green Taxi data in 2020**
✅ 1,734,051

**Q5. Rows in Yellow Taxi data for March 2021**
✅ 1,925,152

**Q6. Correct timezone configuration for New York**
✅ `timezone: America/New_York`

---

## ⏱️ Timezone Configuration (Kestra)

In the Schedule trigger:

```
timezone: America/New_York
```

This ensures workflows run according to New York local time.

---

## 🧪 Execution Notes

* Backfill was run for **2021-01-01 → 2021-07-31**
* Verified that data exists only for these months in 2021
* Each month and taxi type was processed successfully

---

## 📌 Submission

Homework submission form:
[https://courses.datatalks.club/de-zoomcamp-2026/homework/hw2](https://courses.datatalks.club/de-zoomcamp-2026/homework/hw2)

**Due date:** 3 February 2026, 00:59 (local time)

---

## 👩🏽‍💻 Author

**Emmanuel Manuel Junior**
Data Engineer

* GitHub: [github.com/EmmanuelJunuior/De-zoomcamp-module-2)
* LinkedIn: [https://www.linkedin.com/in/emmanuel-manuel-junior-79b886184)
