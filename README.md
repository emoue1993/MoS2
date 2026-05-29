Package already available: numpy
Package already available: pandas
Package already available: matplotlib
Package already available: scikit-learn
Package already available: scipy
Package already available: xgboost
Installing catboost ...
Installing optuna ...
Package already available: shap
Package already available: openpyxl
Installing xlsxwriter ...
Results directory: /content/WCO_ML_Default_vs_Tuned_Results
Please upload your CSV dataset.
combined_OFAT_kinetics_dataset.csv
combined_OFAT_kinetics_dataset.csv(text/csv) - 687 bytes, last modified: 29/05/2026 - 100% done
Saving combined_OFAT_kinetics_dataset.csv to combined_OFAT_kinetics_dataset.csv
Original dataset shape: (34, 5)
Original columns: ['Time_min', 'Temperature_C', 'Molar_Ratio', 'Catalyst_Amount_percent', 'WCO conversion']

Raw dataset preview
Time_min	Temperature_C	Molar_Ratio	Catalyst_Amount_percent	WCO conversion
0	60	100	30	5.0	50.9
1	60	120	30	5.0	80.3
2	60	130	30	5.0	93.1
3	60	140	30	5.0	95.2
4	60	150	30	5.0	97.4

Cleaned dataset shape: (34, 6)

Cleaned dataset preview
Exp_ID	Time_min	Temperature_C	Molar_Ratio	Catalyst_Amount_percent	Conversion_percent
0	1	60	100	30	5.0	50.9
1	2	60	120	30	5.0	80.3
2	3	60	130	30	5.0	93.1
3	4	60	140	30	5.0	95.2
4	5	60	150	30	5.0	97.4

Dataset descriptive statistics
count	mean	std	min	25%	50%	75%	max
Time_min	34.0	53.823529	20.265616	15.0	45.000	60.00	60.0	120.0
Temperature_C	34.0	140.000000	13.706888	100.0	130.000	150.00	150.0	160.0
Molar_Ratio	34.0	30.000000	3.302891	18.0	30.000	30.00	30.0	42.0
Catalyst_Amount_percent	34.0	5.764706	3.296544	1.0	5.000	5.00	5.0	20.0
Conversion_percent	34.0	77.455882	20.769371	22.0	68.225	85.45	93.4	97.4

Train size: (27, 4) Test size: (7, 4)

==========================================================================================
GLOBAL HYPERPARAMETER TUNING: RandomForest
==========================================================================================
Best trial: 55. Best value: 10.1856: 100%
 80/80 [09:53<00:00,  9.98s/it]

==========================================================================================
GLOBAL HYPERPARAMETER TUNING: GBM
==========================================================================================
Best trial: 72. Best value: 7.6787: 100%
 80/80 [02:51<00:00,  3.38s/it]

==========================================================================================
GLOBAL HYPERPARAMETER TUNING: XGBoost
==========================================================================================
Best trial: 77. Best value: 7.71268: 100%
 80/80 [00:59<00:00,  1.22s/it]

==========================================================================================
GLOBAL HYPERPARAMETER TUNING: CatBoost
==========================================================================================
Best trial: 75. Best value: 7.49041: 100%
 80/80 [00:43<00:00,  2.05it/s]

Global tuning results
Model	Best_CV_RMSE_during_tuning	Best_Params
3	CatBoost	7.490415	{"iterations": 740, "learning_rate": 0.2214986...
1	GBM	7.678700	{"n_estimators": 811, "learning_rate": 0.05503...
2	XGBoost	7.712681	{"n_estimators": 1072, "learning_rate": 0.1555...
0	RandomForest	10.185632	{"n_estimators": 873, "max_depth": 14, "min_sa...

Train/Test evaluation: RandomForest | Default
Train/Test evaluation: RandomForest | Tuned
Train/Test evaluation: GBM | Default
Train/Test evaluation: GBM | Tuned
Train/Test evaluation: XGBoost | Default
Train/Test evaluation: XGBoost | Tuned
Train/Test evaluation: CatBoost | Default
Train/Test evaluation: CatBoost | Tuned

==========================================================================================
LOOCV: RandomForest
==========================================================================================

==========================================================================================
LOOCV: GBM
==========================================================================================

==========================================================================================
LOOCV: XGBoost
==========================================================================================

==========================================================================================
LOOCV: CatBoost
==========================================================================================

==========================================================================================
NESTED-CV: RandomForest
==========================================================================================
RandomForest tuned nested fold 1/5
Best trial: 25. Best value: 15.0962: 100%
 40/40 [04:48<00:00,  7.61s/it]
RandomForest tuned nested fold 2/5
Best trial: 35. Best value: 11.9355: 100%
 40/40 [02:36<00:00,  2.98s/it]
RandomForest tuned nested fold 3/5
Best trial: 39. Best value: 9.90137: 100%
 40/40 [04:40<00:00,  9.60s/it]
RandomForest tuned nested fold 4/5
Best trial: 28. Best value: 12.056: 100%
 40/40 [03:28<00:00,  3.65s/it]
RandomForest tuned nested fold 5/5
Best trial: 38. Best value: 12.9014: 100%
 40/40 [03:16<00:00,  4.81s/it]

==========================================================================================
NESTED-CV: GBM
==========================================================================================
GBM tuned nested fold 1/5
Best trial: 34. Best value: 12.9924: 100%
 40/40 [01:26<00:00,  2.70s/it]
GBM tuned nested fold 2/5
Best trial: 25. Best value: 6.74102: 100%
 40/40 [01:26<00:00,  2.55s/it]
GBM tuned nested fold 3/5
Best trial: 30. Best value: 7.06653: 100%
 40/40 [01:22<00:00,  1.44s/it]
GBM tuned nested fold 4/5
Best trial: 38. Best value: 9.33656: 100%
 40/40 [01:37<00:00,  3.47s/it]
GBM tuned nested fold 5/5
Best trial: 38. Best value: 9.62571: 100%
 40/40 [01:01<00:00,  1.84s/it]

==========================================================================================
NESTED-CV: XGBoost
==========================================================================================
XGBoost tuned nested fold 1/5
Best trial: 22. Best value: 12.172: 100%
 40/40 [00:22<00:00,  1.40it/s]
XGBoost tuned nested fold 2/5
Best trial: 37. Best value: 6.52862: 100%
 40/40 [00:28<00:00,  1.26it/s]
XGBoost tuned nested fold 3/5
Best trial: 25. Best value: 7.24226: 100%
 40/40 [00:28<00:00,  1.56it/s]
XGBoost tuned nested fold 4/5
Best trial: 35. Best value: 9.69112: 100%
 40/40 [00:23<00:00,  1.38it/s]
XGBoost tuned nested fold 5/5
Best trial: 27. Best value: 10.0531: 100%
 40/40 [00:21<00:00,  2.35it/s]

==========================================================================================
NESTED-CV: CatBoost
==========================================================================================
CatBoost tuned nested fold 1/5
Best trial: 34. Best value: 11.7891: 100%
 40/40 [00:28<00:00,  1.54it/s]
CatBoost tuned nested fold 2/5
Best trial: 18. Best value: 6.75377: 100%
 40/40 [00:23<00:00,  1.52it/s]
CatBoost tuned nested fold 3/5
Best trial: 15. Best value: 6.81778: 100%
 40/40 [00:26<00:00,  1.78it/s]
CatBoost tuned nested fold 4/5
Best trial: 25. Best value: 10.1827: 100%
 40/40 [00:22<00:00,  1.58it/s]
CatBoost tuned nested fold 5/5
Best trial: 29. Best value: 10.2488: 100%
 40/40 [00:22<00:00,  1.30it/s]
Bootstrap-CV: RandomForest | Default
Bootstrap-CV: RandomForest | Tuned
Bootstrap-CV: GBM | Default
Bootstrap-CV: GBM | Tuned
Bootstrap-CV: XGBoost | Default
Bootstrap-CV: XGBoost | Tuned
Bootstrap-CV: CatBoost | Default
Bootstrap-CV: CatBoost | Tuned

All default-vs-tuned metrics
Model	Hyperparameter_Set	Validation	R2	RMSE	MSE	MAE	MAPE_percent
38	CatBoost	Default	BootstrapCV	0.625952	11.373951	139.826109	8.507341	16.483518
39	CatBoost	Tuned	BootstrapCV	0.713396	9.506499	98.178761	7.129298	11.917648
34	GBM	Default	BootstrapCV	0.596830	11.467505	141.715445	8.634386	15.177742
35	GBM	Tuned	BootstrapCV	0.706626	9.623791	101.106468	7.167431	11.891042
32	RandomForest	Default	BootstrapCV	0.562962	11.855517	150.190113	8.925637	16.113270
33	RandomForest	Tuned	BootstrapCV	0.616489	11.231629	134.549451	8.547899	15.642051
36	XGBoost	Default	BootstrapCV	0.564610	11.892842	150.720493	9.011606	16.121179
37	XGBoost	Tuned	BootstrapCV	0.708490	9.668653	101.128607	7.300756	12.198201
22	CatBoost	Default	LOOCV	0.797491	9.207945	84.786245	6.500901	12.660052
23	CatBoost	Tuned	LOOCV	0.859079	7.681204	59.000898	5.546746	8.816521
18	GBM	Default	LOOCV	0.808441	8.955546	80.201802	6.361180	10.776609
19	GBM	Tuned	LOOCV	0.869160	7.401349	54.779972	5.226332	8.091410
16	RandomForest	Default	LOOCV	0.791164	9.350692	87.435449	6.882390	12.357092
17	RandomForest	Tuned	LOOCV	0.799627	9.159265	83.892130	6.729708	12.113529
20	XGBoost	Default	LOOCV	0.817624	8.738254	76.357086	6.546508	11.581624
21	XGBoost	Tuned	LOOCV	0.848180	7.972708	63.564079	5.800611	9.275770
30	CatBoost	Default	NestedCV	0.756664	10.093543	101.879608	7.023093	14.001059
31	CatBoost	Tuned	NestedCV	0.840138	8.181121	66.930744	5.959286	9.014193
26	GBM	Default	NestedCV	0.782390	9.545107	91.109060	6.758961	12.147643
27	GBM	Tuned	NestedCV	0.835111	8.308767	69.035607	6.235686	10.383014
24	RandomForest	Default	NestedCV	0.692053	11.354789	128.931241	8.130383	14.488545
25	RandomForest	Tuned	NestedCV	0.699197	11.222299	125.939989	8.091954	15.001003
28	XGBoost	Default	NestedCV	0.772970	9.749500	95.052751	7.336898	12.848886
29	XGBoost	Tuned	NestedCV	0.824097	8.581781	73.646965	6.146536	9.796315
13	CatBoost	Default	Test	0.990057	2.368016	5.607501	1.824010	3.558505
15	CatBoost	Tuned	Test	0.995090	1.664118	2.769290	1.498553	2.107856
5	GBM	Default	Test	0.978983	3.442774	11.852690	2.556361	4.851362
7	GBM	Tuned	Test	0.984105	2.994019	8.964149	2.022702	4.286142
1	RandomForest	Default	Test	0.983385	3.061097	9.370317	2.872421	4.993930
3	RandomForest	Tuned	Test	0.977945	3.526771	12.438113	2.787353	5.635862
9	XGBoost	Default	Test	0.874623	8.408821	70.708276	6.125697	11.521953
11	XGBoost	Tuned	Test	0.984786	2.929192	8.580168	2.642611	4.735975
12	CatBoost	Default	Train	0.990036	1.936565	3.750284	1.009568	1.288198
14	CatBoost	Tuned	Train	0.990115	1.928891	3.720619	1.004772	1.276507
4	GBM	Default	Train	0.987437	2.174440	4.728189	1.449812	1.915030
6	GBM	Tuned	Train	0.989536	1.984560	3.938479	1.140100	1.538037
0	RandomForest	Default	Train	0.940031	4.750874	22.570806	3.702149	6.272723
2	RandomForest	Tuned	Train	0.952616	4.223035	17.834028	3.372383	6.014579
8	XGBoost	Default	Train	0.990720	1.868837	3.492553	0.741556	0.912073
10	XGBoost	Tuned	Train	0.990523	1.888647	3.566988	0.874924	1.101014

==========================================================================================
BEST MODEL SELECTED
==========================================================================================
Best model: CatBoost
Selection validation: NestedCV
Best tuned metrics: {'Model': 'CatBoost', 'Hyperparameter_Set': 'Tuned', 'Validation': 'NestedCV', 'R2': 0.8401384822310255, 'RMSE': 8.181121206829394, 'MSE': 66.93074420083364, 'MAE': 5.95928555851042, 'MAPE_percent': 9.014193257523234}
Best hyperparameters: {
    "iterations": 740,
    "learning_rate": 0.22149862489148026,
    "depth": 2,
    "l2_leaf_reg": 1.9945597402304236,
    "bagging_temperature": 5.7092064243428275,
    "random_strength": 2.7523327676679212
}

==========================================================================================
OPTIMUM FEATURE SEARCH AND MAXIMUM PREDICTED CONVERSION
==========================================================================================

Observed best experimental condition
Exp_ID	Time_min	Temperature_C	Molar_Ratio	Catalyst_Amount_percent	Conversion_percent
4	5.0	60.0	150.0	30.0	5.0	97.4

Best trial: 210. Best value: -96.0741: 100%
 1000/1000 [00:28<00:00, 19.28it/s]

Best Optuna optimum condition
Optimization_Method	Time_min	Temperature_C	Molar_Ratio	Catalyst_Amount_percent	Predicted_Conversion_percent	Predicted_Conversion_percent_clipped
0	Optuna_Process_Optimization	74.540144	139.793523	29.382918	4.760094	96.074091	96.074091


Practical rounded optimum condition
Optimization_Method	Time_min	Temperature_C	Molar_Ratio	Catalyst_Amount_percent	Predicted_Conversion_percent	Predicted_Conversion_percent_clipped
0	Practical_Rounded_Optimum	75.0	140.0	29.4	4.76	96.074091	96.074091

Excel summary saved: /content/WCO_ML_Default_vs_Tuned_Results/WCO_ML_default_vs_tuned_complete_summary.xlsx

COMPLETE DEFAULT VS TUNED ML PIPELINE SUMMARY

Dataset size: 34 experiments
Features: Time_min, Temperature_C, Molar_Ratio, Catalyst_Amount_percent
Target: Conversion_percent
Models evaluated: RandomForest, GBM, XGBoost, CatBoost
Removed models: Linear Regression and ElasticNet

Main upgrades in this version:
1. Default hyperparameter evaluation added for all models.
2. Tuned hyperparameter evaluation added using Optuna.
3. Direct Default vs Tuned comparison figures generated for:
   - Train/Test
   - LOOCV
   - Nested-CV
   - Bootstrap-CV
4. Bootstrap-CV includes 95% confidence intervals for R2, RMSE, MSE, MAE, and MAPE.
5. Figure styling enhanced and saved as 600-DPI PNG and optional TIFF.
6. PDF generation removed.
7. Best model selected using tuned Nested-CV RMSE whenever available.
8. Best model interpretation and optimization retained:
   - permutation importance
   - SHAP
   - bootstrap-SHAP stability
   - SHAP interaction matrix
   - PDP/ICE
   - random-search optimization
   - Optuna process optimization
   - counterfactual conditions
   - 3D response surfaces

Best model selected: CatBoost
Selection basis: tuned NestedCV RMSE
Best hyperparameters:
{
    "iterations": 740,
    "learning_rate": 0.22149862489148026,
    "depth": 2,
    "l2_leaf_reg": 1.9945597402304236,
    "bagging_temperature": 5.7092064243428275,
    "random_strength": 2.7523327676679212
}

Observed best experimental condition:
Time = 60.0 min
Temperature = 150.0 °C
Molar ratio = 30.0
Catalyst amount = 5.0 %
Experimental conversion = 97.4 %

ML-predicted practical optimum:
Time = 75.0 min
Temperature = 140.0 °C
Molar ratio = 29.4
Catalyst amount = 4.76 %
Predicted conversion = 96.074 %

Scientific caution:
For small OFAT datasets, the ML optimum should be considered a model-guided experimental suggestion, not a final experimentally confirmed optimum. The predicted optimum must be validated experimentally.

ZIP file created: /content/WCO_ML_default_vs_tuned_complete_results.zip

Pipeline completed successfully.
Main output ZIP: /content/WCO_ML_default_vs_tuned_complete_results.zip
