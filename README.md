#  Watchtronics JMeter Load Test

This project contains a performance testing suite for the Watchtronics e-commerce site using Apache JMeter.

##  Site Tested
[https://watchtronics-123.netlify.app/](https://watchtronics-123.netlify.app/)

## Test Scenarios
- GET Homepage `/`
- Only the homepage (`/`) was tested in this project because other routes like `/products`, `/cart`, etc., returned 404 errors. This happens because the site uses   client-side routing (React Router), and direct access to those paths is not handled by Netlify without a custom `_redirects` file.

## Load Simulated
- 50 Concurrent Users
- 10 Second Ramp-Up
- 1 Loop

## Tools Used
- Apache JMeter
- Summary Report
- Aggregate & Graph Results

## How to Run
```bash
jmeter -n -t jmeter-test-plan.jmx -l results/report.jtl -e -o results/html-report
