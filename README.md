# Intro-to-Health-Analysis
Imperial College Group assignment
Project: The Impact of COVID-19 on Mental Health in the US (Group Assignment)
Group: EDS_B
--- DATA SOURCE DESCRIPTION ---
 Data Series: IPUMS National Health Interview Survey (NHIS)
 Geography: United States (National Level)
 Time Period: 2017 - 2022

--- VARIABLE LIST (IPUMS Names) ---
 1. Demographics: 
    - AGE (Age)
    - SEX (Sex)
    - RACENEW (Race/Ethnicity, post-1997 OMB standards)
    - EDUC (Educational Attainment)
 2. Economic Status:
    - GOTSTAMPFAM (Family received food stamp/SNAP benefits)
 3. Mental Health Outcomes:
    - WORFREQ (Frequency of feeling worried/anxious)
    - DEPFREQ (Frequency of feeling depressed)
 4. Survey Design:
    - YEAR (Survey year)
    - SAMPWEIGHT (Sample Adult Weight for population inference)

--- WEIGHTING STRATEGY ---
 All descriptive statistics (except sample balance) and regression models apply 
 the 'SAMPWEIGHT' variable. This is strictly necessary to:
 1. Account for the NHIS complex survey design (stratification and clustering).
 2. Correct for oversampling and non-response bias.
 3. Ensure results are representative of the US civilian non-institutionalized 
    adult population, rather than just the survey respondents.

--- SAMPLE RESTRICTIONS & EXCLUSIONS ---
 1. Age Restriction: Excluded respondents under 18 (Children universe not asked MH questions).
 2. Time Exclusion: Excluded year 2020 to ensure clear separation between 
    pre-pandemic (2017-2019) and pandemic-era (2021-2022).
 3. Missing Data: Rows with missing values in key control variables (Race, Education, SNAP) were dropped.

--- INSTRUCTIONS FOR REPLICATION ---
 1. Download the data extract from IPUMS NHIS with the variables listed above.
 2. Place the .xml (DDI) and .dat (data) files in the same directory as this script.
 3. Ensure the filename matches the 'read_ipums_micro' function call below.
