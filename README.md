# HoustonKoreanYellowPage
A Probabilistic Identification Using Business Directory Data. Data from dataaxle

# Data Source:
## Data Axle Reference Solution

http://www.referenceusa.com.ezproxy.rice.edu/UsBusiness/Search/Quick/da437f33572b497a8abdae8b548622e9

"Directory information on U.S. and Canadian business, health care, and residential listings. Search by company name, geographic area, business type, SIC code, yellow page listing, revenue, location, number of employees or any combination of the above. In addition to address and phone number, each entry includes officer names and titles, corporate affiliation, business type and size of yellow page advertising. Toll free and fax numbers are given for some companies. " Fondren Library from Rice U.

## ACS Data 5yrs (2024)
Jonathan Schroeder, David Van Riper, Steven Manson, Katherine Knowles, Tracy Kugler, Finn Roberts, and Steven Ruggles. IPUMS National Historical Geographic Information System: Version 20.0 [dataset]. Minneapolis, MN: IPUMS. 2025. http://doi.org/10.18128/D050.V20.0

# Method
Data Axle dataset does not include direct information on owner ethnicity or nationality. I made a probabilistic approach on identifying Korean Businesses

First, a name-based signal is constructed using the last name of the primary executive. Surnames/Last Name can provide meaningful probabilistic information about ethnic identity.

In this coding, I used common Korean Surnames (e.g., Kim, Park, Lee, Choi, Jung, Kwon, and Kang etc). Feel free to adjust the dictionary below.

Conceptually, this approach can be interpreted as a simplified Bayesian classification, where the surname provides a prior probability of ethnic affiliation conditional on observed frequency patterns in the population.

Limitation: This approach has a majoritarian bias. Prior literature (Derby, Dowd, and Mortenson, 2025) shows that this method would overstate the probabilities that non-White individuals are White. In other words, it is hard to detect Korean immigrant descendants with "White individual surnames".

reference:
Kridaraan Komahan, Daniel D. Reidpath, A “Roziah” by Any Other Name: A Simple Bayesian Method for Determining Ethnicity From Names, American Journal of Epidemiology, Volume 180, Issue 3, 1 August 2014, Pages 325–329, https://doi.org/10.1093/aje/kwu129

Derby, E., Dowd, C., & Mortenson, J. (2025). Statistical Bias In Racial and Ethnic Disparity Estimates Using Bayesian Estimation. National Tax Journal, 78(4), 919-938.
