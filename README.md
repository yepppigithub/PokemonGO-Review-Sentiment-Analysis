# Pokémon GO Review Analysis

## 1. Data Collection

- Platform: Google Play Store
- Application: Pokémon GO
- Language: Korean
- Data collection date: [2026.11.5]
- Review publication period: [2018.9.13] to [2026.10.19]
- Total collected reviews: 15,040

## 2. Application Version Information

- Application: Pokémon GO

- App version recorded in the study dataset: Not available

- Version identified at the time of documentation: 0.435.2 (November 2026)

- Review publication period in the analyzed sample: September 13, 2018 – October 19, 2026

The collected Google Play review data did not include application version information for individual reviews. Therefore, the app version used at the time each review was written could not be determined. As a result, differences in user evaluations associated with specific app versions or updates could not be examined.

## 3. Crawling Environment

- Programming language: Python [3.10.16]
- Crawling tool: Selenium [4.39.0]
- Operating system: [Window 11]
- Web browser: [chrome 157.0.8103.51]
- Data collection script: `scripts/crawl_poket.ipynb`

## 4. Data Preprocessing

- Review-level identifiers were extracted from the data-review-id attribute of the Google Play review pages.

- Duplicate reviews were checked using Python based on the review-level identifiers.

- Duplicate detection method: Python-based duplicate check using review IDs (pandas.Series.duplicated()).

- Number of duplicate reviews detected: 0

- Number of duplicate reviews removed: 0

- Number of reviews after preprocessing: 15,040

No duplicate review IDs were detected; therefore, no reviews were removed during the deduplication process.

## 5. Sampling Procedure

A stratified sample was constructed based on star ratings.

| Rating | Original reviews | Analyzed reviews |
|---|---:|---:|
| 1 star | 2,800 | 500 |
| 2 stars | 3,160 | 500 |
| 3 stars | 3,120 | 500 |
| 4 stars | 3,080 | 500 |
| 5 stars | 2,880 | 500 |
| Total | 15,040 | 2,500 |

## 6. Coding Procedure

Eight game evaluation aspects (A01–A08) were defined in Codebook V1.2.

Two human coders independently coded 500 reviews. Disagreements were resolved through discussion and consensus between the two coders.

The remaining 2,000 reviews were coded by Coder A.

The final dataset consisted of 500 consensus-coded reviews and 2,000 reviews coded by Coder A.

## 7. Statistical Analysis

- Descriptive statistics
- Pearson's chi-square tests
- Cramér's V
- Conditional Monte Carlo tests (10,000 simulated tables)
- Benjamini–Hochberg FDR correction

Statistical analysis scripts and aggregated results are provided in this repository.

## 8. Data Availability and Privacy

The repository provides research scripts, coding documentation, and statistical summary tables. The release of review-level data is subject to privacy review and applicable platform data-use conditions.