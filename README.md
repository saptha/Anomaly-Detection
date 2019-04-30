# Anomaly-Detection
Database Performance Anomaly Detection

## Problem Statement
How do we quickly root cause an incident/outage in IT infrastructure?   
We’ve various monitoring systems in place across IT, but when an incident happens in the heterogeneous complex environment it takes too much of time (MTTR) to identify the cause of the incident and resolve it. 

For this problem statement we analyzed all the incidents for a particular given time period and identified high priority incidents in the DBA queue. Identified some of the most critical databases in IT as candidates for this project.   

P.S: While the below prototype was developed at Cisco IT, some of the critical information like hostnames and database names are hidden/modified for security reasons.

## Our approach
We started with an analytical approach based on descriptive statistics and machine language to perform multi-dimensional analysis of historical performance data taken from Oracle’s Automatic Workload Repository (AWR). The goal is to provide a mechanism to visualise realtime, and compare present vs past data to further analyze and alert the stakeholders. The information is collated to proactively identify the problematic area, which will then help us to provide quick root cause of the problem by enabling us to onboard the right support team for the problem identified. This will lead to a faster MTTR.   

Further we can also forecast the future database resource usage and identify the time periods where we need to be on high alert. This is made possible by generating the baselines using the technique of moving averages of the database parameters over a moving window time period. Overall the solution will help us to optimise the end-use experience in IT. 

The approach is based on the following white paper published by KNIME analytics: [KNIME White Paper on Anomaly Detection](https://files.knime.com/sites/default/files/inline-images/Anomaly_Detection_Time_Series_final.pdf) 

Solution is prototyped in R programming. Though this prototype is developed only for database layer, the solution can be extrapolated to other infra layers like network, storage, hosting and applications.

Check out this HTML page generated from RStudio for the prototype. [Solution prototype](index.html) 
