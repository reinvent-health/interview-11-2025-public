# prava-interview-11-2025-public
## Goal
1. Write a simple REST API that computes a provider relevancy score for a single provider
2. (Extra) List providers

## Data
- Our own internal "database" of providers: internal-provider-database.csv
- External third party service returning: https://37fb26dbaf2a.ngrok-free.app/doc

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
