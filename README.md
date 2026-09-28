# Music & Mood Analysis Using Spotify Data

## Overview

This project investigates whether measurable musical characteristics can explain variations in the emotional tone of songs.

Using a large Spotify tracks dataset, we analyze the relationship between:

- Tempo
- Energy
- Danceability
- Valence

Here, **valence** is used as a quantitative measure of the emotional positivity of a song.

## Research Question

> Can musical attributes such as tempo, energy, and danceability significantly explain variations in the emotional tone (valence) of a song?

## Dataset

The dataset contains approximately 114,000 songs and 21 variables.

Each row represents a song and each column represents an audio feature or metadata attribute.

### Variables Used

| Variable | Description |
|---|---|
| Tempo | Speed of the song in BPM |
| Energy | Intensity and activity level of the song |
| Danceability | How suitable a track is for dancing |
| Valence | Measure of musical positivity/emotional tone |

## Methodology

### 1. Data Preprocessing

- Loaded the Spotify dataset in R
- Checked for missing values
- Removed missing observations
- Selected the variables relevant to the research question
- Verified numerical data types

### 2. Exploratory Data Analysis

The following analyses were performed:

- Summary statistics
- Histograms
- Scatter plots
- Correlation matrix
- Box plots
- Comparison of musical variables

### 3. Statistical Analysis

Several statistical methods were used to investigate relationships between musical characteristics and valence:

- Pearson correlation analysis
- Independent two-sample Welch t-test
- Mann–Whitney U test
- Multiple linear regression
- Regression diagnostics
- R-squared and F-statistic analysis

### 4. Hypothesis Testing

For the tempo analysis:

**H₀:** There is no significant association between tempo and valence.

**H₁:** There is a significant association between tempo and valence.

Songs were divided into slow and fast groups using the median tempo.

## Key Findings

The analysis found that:

- Danceability and energy showed positive associations with valence.
- Tempo also showed a statistically significant positive association with valence, although the relationship was weaker.
- Danceability was the strongest predictor of valence among the selected variables.
- Statistical significance was very strong for the tempo-group comparison, while the practical difference between groups was relatively small.

The Welch two-sample t-test produced a p-value below 2.2 × 10⁻¹⁶. The mean valence was approximately 0.482 for the fast-song group and 0.466 for the slow-song group.

## Limitations

- Spotify's valence metric may not completely represent human emotional perception.
- Emotional interpretation of music is subjective.
- The analysis does not include lyrics, cultural factors, or genre-specific effects.
- The very large sample size means that statistically significant results may correspond to relatively small practical effects.

## Future Scope

Possible extensions include:

- Adding additional audio features
- Incorporating genre and metadata
- Performing lyric sentiment analysis
- Applying machine-learning models for mood prediction
- Investigating relationships between music preferences and personality
- Developing mood-based music recommendation systems

## Tools & Technologies

- R
- Statistical Analysis
- Data Visualization
- Multiple Linear Regression
- Hypothesis Testing
- Correlation Analysis

## Repository Structure

```text
spotify-music-mood-analysis/
├── README.md
├── analysis.R
├── music.csv
├── report.pdf
└── plots/
