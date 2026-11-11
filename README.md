# Stage-dependent capacity prediction in doped LNCM cathodes

This notebook accompanies the study of discharge capacity at IC, EC50 and EC100 in single-metal-doped layered Li–Ni–Co–Mn cathodes.

| File | Contents |
| --- | --- |
| `paper_figures.ipynb` | Holdout prediction check, CV and test metrics, and previews of Figures 2–5, S1 and S2 |
| `ncm_dataset.csv` | 213 records, 13 predictors, three targets, dopant identifier and original split metadata |
| `ncm_models.joblib` | Twelve fitted GBR, RF, SVR and GPR estimators, original predictions, signed test-set SHAP values and figure previews |

Use Python 3.12 and install the recorded versions used for inference:

```bash
python -m pip install notebook numpy==2.4.4 pandas==2.3.3 scipy==1.17.1 scikit-learn==1.8.0 joblib==1.5.3
python -m notebook paper_figures.ipynb
```

Keep all four files in one directory and choose **Run All**. Only load the model bundle from this trusted repository. The notebook uses the original 170/43 split and the five recorded validation folds. Columns `sample_index`, `dataset`, `fold`, and `split_order` are metadata. `Dopant_element` is an identifier.

The notebook runs inference with the fitted models and displays previews of the archived manuscript figures. Training and figure-generation sources are in the [original research repository](https://github.com/xyongkang215-ops/ncm-stage-capacity-ml). A public redistribution license has yet to be selected.
