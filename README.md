# Funnel Drop-off Analysis

## Project Overview

This project analyses a user signup and checkout funnel using event-level data. The objective is to measure user progression through each stage of the funnel, calculate conversion rates, identify the largest drop-off point, and provide actionable product recommendations to improve user retention.

---

## Dataset

The dataset contains the following columns:

* **user_id** – Unique identifier for each user
* **step** – Funnel stage reached by the user
* **timestamp** – Time when the event occurred

### Funnel Stages

1. visited_site
2. signup_started
3. details_filled
4. email_verified
5. purchase_completed

---

## Objectives

* Count unique users at each funnel stage.
* Calculate stage-to-stage conversion rates.
* Calculate user drop-offs between stages.
* Identify the biggest funnel leak.
* Visualise the funnel using a bar chart.
* Provide recommendations to improve conversion.

---

## Tools & Technologies

* Python
* Pandas
* Matplotlib
* Google Colab

---

## Methodology

1. Loaded the dataset into Pandas.
2. Checked the dataset structure and verified there were no duplicate records.
3. Grouped the data by funnel stage and counted unique users.
4. Calculated conversion rates between consecutive stages.
5. Calculated drop-off counts and percentages.
6. Identified the stage with the highest user loss.
7. Visualised the results using a bar chart.

---

## Results

| Funnel Stage       | Unique Users | Conversion Rate (%) |
| ------------------ | -----------: | ------------------: |
| visited_site       |          200 |              100.00 |
| signup_started     |          150 |               75.00 |
| details_filled     |           96 |               64.00 |
| email_verified     |           52 |               54.17 |
| purchase_completed |           44 |               84.62 |

### Biggest Funnel Leak

* **Stage:** signup_started → details_filled
* **Users Lost:** 54
* **Drop-off Percentage:** 36.00%

---

## Recommendation

The largest drop-off occurs between the **signup_started** and **details_filled** stages. This indicates that users may experience friction while entering their details. Simplifying the form, reducing unnecessary input fields, improving validation messages, and optimising the user experience at this step can help increase completion rates and improve overall conversions.

---

## Project Structure

```text
funnel-dropoff-analysis/
│── Funnel_Dropoff_Analysis.ipynb
│── funnel_events_sample.csv
└── README.md
```

---

## Conclusion

The analysis identified the most significant loss of users between the **signup_started** and **details_filled** stages. Focusing product improvements on this step has the greatest potential to increase the number of users who successfully complete the funnel.

---
