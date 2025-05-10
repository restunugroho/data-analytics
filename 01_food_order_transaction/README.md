# 🍽️ Synthetic Food Order Transaction Analysis

This repository contains a synthetic dataset that simulates food order events from both **mobile app** and **offline (walk-in)** orders. The dataset is designed to mimic real-world transactional data for analytical and operational insights.

---

## 📦 Dataset Description

Each row in the dataset represents an **event** in the lifecycle of a food order, identified by a unique `order_id`.

### 🔑 Key Columns:
- `order_id`: Unique identifier for each order.
- `outlet_name`: The outlet where the order was placed (only available during order creation).
- `location`: The location name of the outlet (only available during order creation).
- `menu_item`: Item that was ordered (only available during order creation).
- `order_type`: Type of order (e.g., apps, offline) — available only when status is `created`.
- `status`: Current status of the order.
- `timestamp`: Timestamp indicating when the event occurred.

> ℹ️ Note: Fields such as `outlet_name`, `location`, `menu_item`, and `order_type` are **only populated** for events with status = `created`. For all other statuses, only `order_id`, `status`, and `timestamp` are recorded.

---

## 🧠 Analytical Challenges

This dataset enables exploration of several real-world business questions and operational insights, such as:

### 1. 📊 Hourly Order Trends
- Build an **hourly aggregation of order counts**, grouped by:
  - `location`
  - `menu_item`
- Analyze patterns to uncover **daily trends** and **seasonality** (e.g., peak hours, weekday vs weekend behavior).

### 2. ⏱️ Order Status Duration Analysis
- Calculate **duration statistics** (mean, median, Q1, Q3) for time spent in each `status` stage.
- Group the analysis by:
  - `location`
  - `menu_item`
  - Day of the week (weekday/weekend)
  - Holiday vs non-holiday (if applicable)
  
**Can you solve the challenges using SQL ?**

**Upload the data to BigQuery, then solve using SQL.**

## 📬 Contact

For questions, feedback, or collaboration, feel free to reach out :
Restu Nugroho
https://www.linkedin.com/in/restu-nugroho-11221270/
restuv13@gmail.com

---

*Happy analyzing!*
