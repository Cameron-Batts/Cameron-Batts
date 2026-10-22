# Portfolio Validation Review

Updated October 22, 2026. This pass covered the 19 remaining analysis projects linked from the portfolio. Twelve revised workflows were executed, one project had its traditional baselines verified with BERT training prepared, and six SAS projects received static-export reviews. Aviation source CSV calculations were also rerun.

Results describe the tested workflow and evidence available, rather than certifying production performance. Historical outputs are retained separately where the revised analysis changed preprocessing or evaluation.

## Remaining-project review

| Project | Evidence status | Record |
| --- | --- | --- |
| [Benford-Iran-Election](https://github.com/Cameron-Batts/Benford-Iran-Election) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Benford-Iran-Election/blob/main/Reports/validation_results.json) |
| [Book-Topic-Modeling-and-Financial-NER](https://github.com/Cameron-Batts/Book-Topic-Modeling-and-Financial-NER) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Book-Topic-Modeling-and-Financial-NER/blob/main/reports/validation_results.json) |
| [Housing-Outlier-Regression](https://github.com/Cameron-Batts/Housing-Outlier-Regression) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Housing-Outlier-Regression/blob/main/Reports/validation_results.json) |
| [Housing-Price-Timeseries](https://github.com/Cameron-Batts/Housing-Price-Timeseries) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Housing-Price-Timeseries/blob/main/Reports/validation_results.json) |
| [Loan-Default-Decision-Tree](https://github.com/Cameron-Batts/Loan-Default-Decision-Tree) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Loan-Default-Decision-Tree/blob/main/Reports/validation_results.json) |
| [Loan-Default-Logistic](https://github.com/Cameron-Batts/Loan-Default-Logistic) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Loan-Default-Logistic/blob/main/Reports/validation_results.json) |
| [Mall-Customer-Segmentation](https://github.com/Cameron-Batts/Mall-Customer-Segmentation) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Mall-Customer-Segmentation/blob/main/Reports/validation_results.json) |
| [Movie-Review-Sentiment-BERT](https://github.com/Cameron-Batts/Movie-Review-Sentiment-BERT) | Baselines verified; BERT training pending | [Validation](https://github.com/Cameron-Batts/Movie-Review-Sentiment-BERT/blob/main/reports/validation_results.json) |
| [Multiclass-Sentiment-Classification](https://github.com/Cameron-Batts/Multiclass-Sentiment-Classification) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Multiclass-Sentiment-Classification/blob/main/reports/validation_results.json) |
| [NYC-Flight-Delay-Analysis](https://github.com/Cameron-Batts/NYC-Flight-Delay-Analysis) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/NYC-Flight-Delay-Analysis/blob/main/Reports/validation_results.json) |
| [Regression-Classification-Metrics](https://github.com/Cameron-Batts/Regression-Classification-Metrics) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Regression-Classification-Metrics/blob/main/Reports/validation_results.json) |
| [SAS-Customer-Retail-Analysis](https://github.com/Cameron-Batts/SAS-Customer-Retail-Analysis) | Static export review | [Validation](https://github.com/Cameron-Batts/SAS-Customer-Retail-Analysis/blob/main/Reports/validation_results.json) |
| [SAS-Facility-Products](https://github.com/Cameron-Batts/SAS-Facility-Products) | Static export review | [Validation](https://github.com/Cameron-Batts/SAS-Facility-Products/blob/main/Reports/validation_results.json) |
| [SAS-Insight-Toys](https://github.com/Cameron-Batts/SAS-Insight-Toys) | Static export review | [Validation](https://github.com/Cameron-Batts/SAS-Insight-Toys/blob/main/Reports/validation_results.json) |
| [SAS-Megacorp-Acquisition-Analysis](https://github.com/Cameron-Batts/SAS-Megacorp-Acquisition-Analysis) | Static export review | [Validation](https://github.com/Cameron-Batts/SAS-Megacorp-Acquisition-Analysis/blob/main/Reports/validation_results.json) |
| [SAS-Sports-Product](https://github.com/Cameron-Batts/SAS-Sports-Product) | Static export review | [Validation](https://github.com/Cameron-Batts/SAS-Sports-Product/blob/main/Reports/validation_results.json) |
| [SAS-US-Aviation-Industry-Trends](https://github.com/Cameron-Batts/SAS-US-Aviation-Industry-Trends) | Static export review | [Validation](https://github.com/Cameron-Batts/SAS-US-Aviation-Industry-Trends/blob/main/Reports/validation_results.json) |
| [Sentiment-Analysis-Comparison](https://github.com/Cameron-Batts/Sentiment-Analysis-Comparison) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Sentiment-Analysis-Comparison/blob/main/reports/validation_results.json) |
| [Word-Embedding-Comparison](https://github.com/Cameron-Batts/Word-Embedding-Comparison) | Revised workflow rerun | [Validation](https://github.com/Cameron-Batts/Word-Embedding-Comparison/blob/main/reports/validation_results.json) |

## Important findings

- The loan tree achieved high default recall with many false positives; its revised test precision was 11.79% and specificity 8.02%. Logistic regression at a 0.5 threshold missed all defaults. The reports show these tradeoffs explicitly.
- The revised housing forecast comparison favored VAR on one 24-month historical window. This is a separate backtest, not a claim of general forecasting superiority.
- Mall segmentation reproduced six clusters across all six searches. PCA retained 77.57% of variance with two components; no marketing outcome or cluster stability was validated.
- Book LDA training-corpus scores and raw-span NER were executed. Neither is a held-out accuracy benchmark.
- Six SAS PDFs were audited as exports. Native report interactions and forecasts were not represented as tested.

## Earlier completed work

| Project | Evidence available |
| --- | --- |
| [Bank Marketing](https://github.com/Cameron-Batts/Bank-Marketing-Prediction) | All 16 code cells executed; historical and rerun payoff figures kept separate. |
| [Retail Sales](https://github.com/Cameron-Batts/Retail-Sales-Analysis) | Included-data workflow executed and aggregation/join checks documented in the earlier pass. |
| [LASSO](https://github.com/Cameron-Batts/Lasso-Regression-Pipeline) | All 13 code cells executed; selected indices matched all ten generating predictors. |
| [SVM](https://github.com/Cameron-Batts/Svm-Classification-Feature-Engineering) | All 18 code cells executed and six figures regenerated; perfect scores labeled as fitting-data scores. |
| [Financial BERT](https://github.com/Cameron-Batts/Financial-Sentiment-BERT-Finetuning) | Owner-supplied MPS export records both ten-epoch runs. Dataset hash, aggregate arithmetic and checkpoint selection checked; raw predictions/weights were not independently inspected. |
| [Airline LLM](https://github.com/Cameron-Batts/Airline-Refund-LLM-Evaluation) | All eight offline code cells and ten parser checks passed. Live model behavior was not re-evaluated. |
| [Tableau](https://github.com/Cameron-Batts/Tableau-Sales-Dashboard) | Owner reported both workbooks load and respond to manual interactions; source spreadsheet totals were independently recomputed. Refresh and full extract/KPI reconciliation remain unverified. |
| [Power BI](https://github.com/Cameron-Batts/Power-BI-Healthcare-Operations) | Owner confirmed functionality. Original PBIX, model and source tables were not supplied for independent verification. |

## Remaining validation limits

- **Movie-review BERT:** a new two-epoch training run still requires MPS/CUDA. The main notebook now supports MPS, fixes the model/data revisions and initializes the binary head after setting the seed. Its final cell exports `reports/gpu_rerun_metrics.json`. [Open the notebook](https://github.com/Cameron-Batts/Movie-Review-Sentiment-BERT/blob/main/notebooks/movie_review_sentiment_bert.ipynb).
- **SAS and Power BI:** deeper calculation, refresh and native-report validation requires missing original definitions/models and appropriate source data.
- **Archived examples:** absent vehicle/bank fitted artifacts, historical R demonstrations and optional pretrained Google News results are not presented as reproduced merely because a revised/default workflow ran.
- **Evaluation quality:** single splits, corpus overlap, subjective labels, illustrative payoff assumptions and missing provenance remain disclosed in each project. No production, causal or financial return is claimed.

## Scope

GitHub Skills exercises, course starter apps, infrastructure samples and repositories not linked as analysis projects were outside this portfolio pass. Raw local text datasets and model weights were excluded from the publication files.
