# Dataset: physiological, ocular and braking measures in a four-cohort driving-simulator study

## Related manuscript
Age, Driving Experience, and Cognitive Load in Physiological, Ocular, and Braking
Profiles: A Four-Cohort Driving-Simulator Comparison (under review).

## Contents
| File | Description |
|---|---|
| `data_long.csv` | Main dataset, long format: one row per participant x condition (52 x 4 = 208 rows; 36 columns). |
| `participants.csv` | One row per participant: group, age, sex, years of driving experience (52 rows). |
| `data_dictionary.csv` | Variable dictionary: meaning, unit, coding and notes. |
| `README.md` | This file. |

## Design
- Four groups of 13 participants (N = 52): young novice (YN), young experienced (YE),
  elderly novice (EN) and elderly experienced (EE). Age ranges: YN 20–30, YE 22–36,
  EN 65, EE 60–65 years; novices held a licence for <3 years, experienced drivers for
  ≥10 years.
- Within-subject cognitive-load manipulation (counterbalanced): baseline, 0-back,
  1-back and 2-back (auditory n-back).
- Each condition was a 7.13-km simulated highway drive in a fixed-base simulator with
  braking stimuli; ECG and eye movements were recorded continuously.
- Participant-level variables (age, sex) are in `participants.csv`, not in the long table.

## Measures deposited
- **Cardiac**: mean heart rate and its SD, IBI, SDNN, RMSSD, pNN50, LF and HF power,
  LF/HF ratio, Poincaré SD1/SD2.
- **Ocular**: blink count, rate and mean duration; fixation count, mean duration, total
  duration and time ratio; fixation sample count; saccade count and mean duration;
  tracking gaps; pupil diameter (mean and SD); mean, maximum and SD of gaze velocity;
  mean and SD of horizontal and vertical gaze position.
- **Behavioural**: brake reaction time to the braking stimulus.

## Session exclusions
The segment-quality flags of the source recordings are not part of this deposit, so the
sessions that failed the quality check are listed here explicitly:

- Excluded from HRV analyses (segment flagged as not usable): P30 (1-back), P31 (0-back), P32 (0-back), P33 (0-back).
- Excluded from eye-tracking analyses (segment flagged as not usable): P40 (1-back).

All other missing values arise because the corresponding segment was not recorded.

## Missing data
Rows with missing values (count):
| column | missing rows |
|---|---|
| `blink_duration_mean_ms` | 10 |
| `blink_rate_per_min` | 10 |
| `brake_reaction_time_s` | 4 |
| `fixation_duration_mean_ms` | 9 |
| `fixation_sample_count` | 4 |
| `fixation_time_ratio_pct` | 8 |
| `fixation_total_duration_s` | 9 |
| `gap_count` | 4 |
| `gaze_velocity_max_deg_s` | 8 |
| `gaze_velocity_sd_deg_s` | 8 |
| `gaze_x_mean_pct` | 4 |
| `gaze_x_sd_pct` | 4 |
| `gaze_y_mean_pct` | 4 |
| `gaze_y_sd_pct` | 4 |
| `hr_sd_bpm` | 4 |
| `lf_hf_ratio` | 4 |
| `lf_power` | 4 |
| `pupil_diameter_mean_mm` | 7 |
| `pupil_diameter_sd_mm` | 7 |
| `saccade_duration_mean_ms` | 9 |

## Points to confirm before the dataset is published
1. **Units of `lf_power` and `hf_power`** (absolute ms² vs normalised) must be stated in
   the dictionary before upload.
2. **Brake reaction time and heart-rate SD carry few distinct values**
   (53 and 67 distinct values across 204 non-missing rows). If this
   reflects the recording resolution, document it here; otherwise re-export as for the
   other cardiac measures.
3. **Sample sizes**: the manuscript reports per-measure analysis samples (for example
   heart rate n = 38, brake reaction time n = 29) that are smaller than this file's
   coverage (208 rows / 52 participants). State the exclusion rules (including the
   sessions listed above) so that the analyses can be reproduced.
4. **NASA-TLX ratings are not included.** If they are to be shared, they must be
   rebuilt from the original questionnaires (an earlier compilation repeated values
   across participants).
5. **Age and sex are not in the long-format table**; both appear in `participants.csv`
   (needed for Table 2). If they are not to be shared at all, remove those columns.
6. **Age text in the manuscript**: the manuscript currently states 25–40 and
   ≥65 years, whereas this dataset and Table 2 show 20–36 and 60–65 years.
   These must agree before submission.

## Licence
CC BY 4.0 (to be confirmed by the authors).

## Citation
[Authors]. ([Year]). Dataset for "Age, Driving Experience, and Cognitive Load in
Physiological, Ocular, and Braking Profiles: A Four-Cohort Driving-Simulator
Comparison" [Data set]. [Repository]. https://doi.org/[DOI]

## Contact
[Corresponding author name, affiliation, email]
