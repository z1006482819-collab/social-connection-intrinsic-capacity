# Data Extraction Codebook

This codebook is designed for the systematic review examining associations between social connection and intrinsic capacity (IC) among adults aged 50 years and older.

## Unit of analysis

Use **one row per reported association/effect estimate**, not necessarily one row per paper. A single study may therefore occupy multiple rows when it reports multiple social connection constructs, IC outcomes/domains, models, subgroups, or follow-up waves.

Assign a stable `study_id` so multiple rows from the same study can be linked.

## Recommended variables

### 1. Study identification
| Variable | Description |
|---|---|
| study_id | Stable short ID, e.g. Yue_2025 |
| citation | First author and year |
| doi | DOI where available |
| country | Country/setting |
| dataset_cohort | Named cohort/dataset if applicable |
| publication_year | Year of publication |

### 2. Study design and sample
| Variable | Description |
|---|---|
| study_design | Cross-sectional / longitudinal / cohort / other |
| waves_followup | Number of waves or follow-up duration |
| sample_size | Analytic sample size |
| age_eligibility | Study age eligibility |
| age_mean | Mean age if reported |
| age_sd | SD if reported |
| female_percent | Percentage female/women if reported |
| setting | Community / rural / urban / other |
| population_notes | Relevant population characteristics |

### 3. Social connection exposure
| Variable | Description |
|---|---|
| sc_construct | Loneliness / social isolation / social participation-engagement / social network |
| sc_measure | Instrument, index, or operational definition |
| sc_variable_type | Continuous / categorical / score / other |
| sc_reference | Reference category where relevant |
| sc_direction | Higher score = better or poorer social connection |
| exposure_timing | Baseline/concurrent/other |

Do not collapse loneliness, social isolation, social participation, and social networks into one undifferentiated exposure.

### 4. Intrinsic capacity outcome
| Variable | Description |
|---|---|
| ic_outcome | Overall IC / locomotion / cognition / psychological / vitality / sensory |
| ic_measure | Instrument or method used to construct IC |
| ic_variable_type | Continuous / impaired-intact / latent class / transition / other |
| ic_direction | Higher score = better or poorer IC |
| outcome_timing | Baseline/follow-up/time point |

### 5. Effect estimate
| Variable | Description |
|---|---|
| effect_measure | OR / HR / RR / beta / mean difference / correlation / other |
| effect_estimate | Numeric estimate |
| ci_lower | Lower 95% CI |
| ci_upper | Upper 95% CI |
| p_value | P value if reported |
| model | Unadjusted / adjusted / final model |
| covariates | Adjustment variables |
| association_direction | Positive / negative / null or non-significant / mixed |
| statistically_significant | Yes / No / unclear |

Preserve the authors' reported effect measure. Do not convert different effect measures into a common metric unless a later meta-analysis justifies and documents the conversion.

### 6. Subgroups and interpretation
| Variable | Description |
|---|---|
| subgroup | Overall sample / sex / age / rurality / birthplace / other |
| subgroup_value | Specific subgroup label |
| authors_interpretation | Brief faithful summary of authors' interpretation |
| reviewer_notes | Extraction notes, ambiguity, limitations |
| reverse_direction_flag | Yes if IC is modelled as exposure/predictor rather than social connection |
| eligible_for_primary_synthesis | Yes / No / unclear |

## Coding principles

1. Keep the four social connection constructs distinct.
2. Keep overall IC and individual IC domains distinct.
3. Record study direction explicitly. A paper modelling IC as the predictor and social participation as the outcome should not silently be treated as evidence for social connection → IC.
4. Separate adjusted and unadjusted estimates when both are extracted.
5. Record subgroup estimates as separate rows.
6. Use `NA` for genuinely unreported/not applicable values rather than guessing.
7. Keep original numeric effect estimates exactly as reported during extraction; derived variables can be created later in analysis code.
8. Do not code a causal effect from observational associations.

## Planned analytical uses

This structure can support:
- counts of studies by social connection construct and IC outcome;
- evidence maps across constructs and IC domains;
- study-design and geographical summaries;
- subgroup summaries;
- identification of evidence gaps;
- forest plots or meta-analysis only where effect measures, exposures, outcomes, and study designs are sufficiently comparable.

## Important note

This is a working extraction framework. It should be reconciled with the final review protocol, eligibility criteria, supervisor guidance, and any required risk-of-bias tool before the final extraction begins.
