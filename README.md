# Uber Revenue Booking Insights (2022 - 2024)
This project analyzes Uber's ride and booking performance from 2022 to 2024, focusing on %YoY or %MoM revenue trends, customer behavior patterns, cancellation reasons, high demand areas with no driver availability, and operational efficiency. The report is built entirely in Power BI, using a robust star schema data model and interactive visuals.

# Report Screenshots
<img width="1872" height="1022" alt="image" src="https://github.com/user-attachments/assets/2623ad3c-c654-4e66-8122-f463afa0648f" />
<br></br>
<br></br>
<img width="1870" height="1014" alt="image" src="https://github.com/user-attachments/assets/85ca8c47-17a5-4bb4-a8f4-c71325a4f6a7" />
<br></br>
<br></br>
<img width="1869" height="1012" alt="image" src="https://github.com/user-attachments/assets/0d2a3707-8d80-4671-a807-e6f6328ccc2c" />
<br></br>
<br></br>
<img width="1867" height="1023" alt="image" src="https://github.com/user-attachments/assets/9ecf3299-971d-42e3-925c-0437eff2f002" />
<br></br>
<br></br>
<img width="1857" height="786" alt="image" src="https://github.com/user-attachments/assets/f48c754e-c508-43c2-aaac-8aaab231b5b3" />
<br></br>
<br></br>
<img width="1862" height="1021" alt="image" src="https://github.com/user-attachments/assets/e3a488d3-d1f8-412b-a45e-bdfbd3cbe06d" />

# Data Dictionary
Below are the data schemas of the 2 datasets containing the following columns:

+ **Booking table**

**Note**: Originally, the dataset only provides booking records in 2024. However, building a dashboard/report with only 1-year worth of data means minimal analysis can be done, resulting a relatively plain and shallow dashboard. Therefore, using existing booking records in 2024, data for the year 2022 and 2023 are artificially generated via extrapolation and randomization for the sole purpose of making data more diverse and populated over a larger timeframe to support dashboarding.
  
| Feature | Description | Example Value |
| :--------: | :------: | :--------: |
| Date | Date of the booking | 01/31/2022 |
| Time | Time of the booking | 17:17:25 |
| Booking ID | Unique identifier for each booking ride | CNR5884300 |
| Booking Status | Status of booking (Completed, Cancelled by Customer, Cancelled by Driver, etc.) | No Driver Found |
| Customer ID | Unique identifier for customers | CID1982111 |
| Vehicle Type | Type of vehicle (Go Mini, Go Sedan, Auto, eBike/Bike, UberXL, Premier Sedan) | Auto |
| Pickup Location | Starting location of the ride | AIIMS | 
| Drop Location | Destination location of the ride | Khan Market |
| Avg VTAT | Average time for driver to reach pickup location (in minutes) | 5.5 |
| Avg CTAT | Average trip duration from pickup to destination (in minutes) | 14 |
| Cancelled Rides by Customer | Customer-initiated cancellation flag | 1 |
| Reason for cancelling by Customer | Reason for customer cancellation | Wrong Address |
| Cancelled Rides by Driver	| Driver-initiated cancellation flag | 0 |
| Driver Cancellation Reason	| Reason for driver cancellation | Personal & Car related issues |
| Incomplete Rides	| Incomplete ride flag | 1 |
| Incomplete Rides Reason	| Reason for incomplete rides | Vehicle Breakdown |
| Booking Value	| Total fare amount for the ride | 237 | 
| Ride Distance	| Distance covered during the ride (in km) | 5.73 |
| Driver Ratings	| Rating given to driver (1-5 scale) | 5 |
| Customer Rating	| Rating given by customer (1-5 scale) | 2.5 |
| Payment Method	| Method used for payment (UPI, Cash, Credit Card, Uber Wallet, Debit Card) | Cash |

+ **Customer table**

**Note**: The originally provided data source only contains the *Booking* table with only the *Customer ID* relating to customers. No personally identifiable information were disclosed. However, this means we are left with only the fact table with no dimension tables to filter through the fact table. While analysis can still be done, however, the depth of the analysis will be severely limited. Therefore, customer data for the features shown in the table below are artificially generated. Any resemblance to actual persons is purely coincidental.

| Feature | Description | Example Value |
| :--------: | :------: | :--------: |
| Customer ID | Unique identifier for customers | CID1982111 |
| Gender | Customer's gender | Female |
| DOB | Customer's date of birth | 10/15/1995 | 
| First Name | Customer's first name | Alice |
| Last Name	| Customer's last name | Lee |
| Phone Number	| Customer's phone number | 04425 708 360 |
| Loyalty tier	| Customer's loyalty level (Bronze, Silver, Gold) | Silver | 
| Marketing Segment	| Segment classification based on ride frequency | Frequent Rider |
