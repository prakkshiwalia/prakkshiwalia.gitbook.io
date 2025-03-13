---
description: >-
  As a Product Manager, we often rely on A/B testing to make data-driven
  decisions.
---

# Lib: A/B Testing with Fake User Data

**Objective of the project:**

We'll create a **fake dataset of 20 users** participating in an **A/B test** to analyze how they interact with a product. The dataset will include user demographics and engagement metrics. Then, using **Pandas and NumPy**, we'll analyze this dataset to understand user behavior and determine if the A/B test had any significant impact.

1. **Generate fake user data (20 users)**
   * Each user will belong to **either Group A (Control) or Group B (Variant)**.
   * Data will include: **User ID, Age, Country, Session Duration, Click-Through Rate (CTR), Conversion Rate, Revenue Generated, and Test Group.**
2. **Analyze the dataset using Pandas and NumPy**
   * Calculate **summary statistics** for user engagement (session duration, CTR, conversion rate).
   * Compare **Group A vs. Group B** to determine if the variant improves performance.
   * Identify **outliers** and their potential impact.
3. **Interpret Results**
   * Use statistical analysis to **conclude whether the test group (B) performed better than control (A)**.
   * Provide actionable insights based on the findings.
