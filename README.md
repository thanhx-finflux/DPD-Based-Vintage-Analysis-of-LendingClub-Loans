# DPD-Based-Vintage-Analysis-of-LendingClub-Loans
This repository analyzes delinquency behavior over the life of LendingClub loans. Compute Months on Book (MOB) for each loan and build delinquency curves over time.

## Ojective
- Analyze delinquency behavior over the life of LendingClub loans
- Build DPD-based vintage curves (1-15, 16-30, 31-120, 120+ DPD) by months on book (MOB)
- Identify performance window, default build-up, and portfolio trends

  ## Data
  - Public LendingClub loan data on Kaggle
  - Fields used: issue_d, loan_status,...

  ## Methodology
  - Convert issue_d to month on book (MOB) using a fixed snapshot data (2019-03)
  - Map loan_status into approximate DPD buckets

    <img width="1329" height="699" alt="Image" src="https://github.com/user-attachments/assets/f930ef9d-e9a4-44c5-a4b0-c4bd97d65021" />

    <img width="1311" height="699" alt="Image" src="https://github.com/user-attachments/assets/a5000348-fcbd-445a-af8c-cbc3d444b4d4" />

    <img width="1320" height="699" alt="Image" src="https://github.com/user-attachments/assets/a760abc8-7a7f-42d0-b443-19683ff6fcc5" />

    <img width="1298" height="699" alt="Image" src="https://github.com/user-attachments/assets/fb8c9f60-053f-4284-8d20-31a024b553ce" />

    <img width="763" height="545" alt="Image" src="https://github.com/user-attachments/assets/7bb1913a-4124-41b6-aa23-783797019323" />

    <img width="700" height="1469" alt="Image" src="https://github.com/user-attachments/assets/618149ab-0390-4e1f-b4c3-4807ee7b65db" />

<img width="703" height="1469" alt="Image" src="https://github.com/user-attachments/assets/e4ede715-5c40-4c65-a30f-9d2ea38c6bb4" />

## Key Findings
- DPD 0 Vintage Curve shows the percentage of loans that are in good standing, starting from 99% at month 4 and gradually decreasing to around 80% to 82% at 33 months on book (MOB). This indicates that as loans age, a greater percentage of them experience delinquency or default. Declines from 99% to 82%, which means about 18% of loans experience some level of delinquency by month 60. It is extremely realistic that as loans age, the likelihood of delinquency increases.
- 1-15 DPD peaks early at around 0.8% at month 12, then gradually declines to around 0.1% at month 60. This is normal as early delinquencies are often resolved quickly.
- 16-30 DPD peaks at around 0.4% at month 15, then declines to near 0% by month 60. Shows portfolio stabilization.
- 31-120 DPD peaks at around 2.2% at month 19, then declines to around 0.2% by month 60. In the early months near snapshot, serious delinquencies rise as some borrowers struggle to repay, but over time, many of these loans either recover or are charged off, leading to a decline in this category.
- DPD 121+ Vintage Curve shows the percentage of loans that have defaulted (121+ days past due), starting from 0% at month 4, peaks at around 18% at month 40,  and fluctuates to around 17% from month 40 to month 60. This indicates that as loans age, a higher percentage of them eventually default. The increase from 0% to 17% indicates that about 17% of loans default by month 60, a realistic trend in loan portfolios, as some borrowers inevitably face financial difficulties over time.

## Tools

Jupyter Notebook, Python (Pandas, Matplotlib, Seaborn)
## Contact

Thanh Xuyen, Nguyen

LinkedIn: [xuyen-thanh-nguyen-0518](https://www.linkedin.com/in/xuyen-thanh-nguyen-0518/)

Email: thanhxuyen.nguyen@outlook.com
