# prava-interview-11-2025-public
## Goal
1. Write a simple REST API that computes a provider relevancy score for a single provider - `GET providers/:provider_id`
2. List providers - `GET providers/`

## Data
- Our own internal "database" of providers: internal-provider-database.csv - consider the index in the csv file as the provider_id
- You will use an external third party service that you can consider as a "global" public registry of providers: https://37fb26dbaf2a.ngrok-free.app/docs

## Relevancy score rule
Score out of 5 based on 5 criteria
- Age
  - 20-25: 0.25
  - 25-45: 1
  - 45-60: 0.25
- Years of experience
  - less than 3 years: 0
  - between 3 and 10 years: 0.5
  - more than 10 years: 1
- Board certified
  - false: 0
  - true: 1
- Hourly pay rate
  - less than 100: 1
  - betwen 100 and 150: 0.75
  - between 150 than 200: 0.5
  - more than 200: 0.25
- Distance from hq
  - less than 25km: 1
  - between 25 and 50: 0.5
  - more than 50: 0
