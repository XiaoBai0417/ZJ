# Zhejiang healthcare accessibility: code and key data

This package contains the main Python code and processed data supporting the multimodal healthcare accessibility analysis in Zhejiang Province.

## Contents

- `code/`: analysis, figure-generation and table-generation scripts.
- `data/health_place_grid_table.parquet`: central processed grid dataset.
- `data/figure10_*`: accessibility-regime source data.
- `data/figure11_*`: spatial-validation and SHAP results.
- `tables/`: five principal statistical tables and the regime-planning response table.
- `requirements.txt`: tested Python package versions.

## Key AI results

The random-forest surrogate classifier achieved an accuracy of 0.833, a macro-F1 score of 0.779 and Cohen's kappa of 0.732 under five-fold spatial block validation. Public-transit and walking indicators jointly accounted for 68.1% of global SHAP importance.

## Use

Install the packages in `requirements.txt`, then update the relative input paths in the scripts if complete map reproduction is required. Raw navigation surfaces, healthcare POIs, population rasters, administrative boundaries, terrain data and satellite imagery are not included because of size or third-party access conditions.

The Type A-D labels are planning-oriented regimes. The random forest is an explainable surrogate used to diagnose regime differentiation and should not be interpreted as a causal model.

Before public release, reconcile the reported facility total (20,759 versus 20,761) and the primary-care walking-threshold population estimate (18.90 versus 20.09 million).
