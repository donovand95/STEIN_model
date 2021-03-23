'''
STEIN_model

MODEL INFORMATION

Quantifying erosion rates in high mountain areas is not straightforward due to the stochastic processes which often dictate alpine erosion rates. Among those, frost-cracking and permafrost thaw both contribute to erosion rates in cold, high-alpine regions, but the relative contributions of both are not well-constrained. The STEIN model (stochastically-eroding in situ cosmogenic nuclide model) is a 1D numerical model that simulates surface concentrations of cosmogenic Be-10, C-14, and He-3, alongside the bedrock thermal field, under variable erosion rates and types. Simulations can evolve under the following erosion types: “stochastic,” “uniform,” "episodic," and "no erosion." Each non-uniform erosion scenario is accompanied by a uniformly-eroding output at the Be-10 derived erosion rate.

To run the model, open and run the code "master_script_STEIN." The scripts will generate a sequence of output files. The model can take some time for each individual evaluation, depending on the integration time (total model time) input. Figures corresponding to those in the publicaiton can be generated using the "plotting_functions" script. A test dataset from which figures in the accompanying publication are generated is included in the folder "test_dataset."

Files in the test dataset are divided according to the scenario type. Files within the correction_test_dataset folder and stochastic_outputs folders are “Scenario Output Files”, the following row/column naming conventions apply:

Rows:
Index corresponds to years elapsed (yr)
Columns:
0: Surface C-14 Conc. (at g-1) ;
1: Surface Be-10 Conc. (at g-1) ;
2: Surface C-14 / Be-10 Ratio ;
3: Surface He-3 Conc. (at g-1) ; 
4. Surface He-3 Retention (%) ;
5. Erosion Event Depth (cm) ;
6. Surface C-14 Conc. (at g-1) ;
7. Surface Be-10 Conc. (at g-1) ;
8. Surface C-14 / Be-10 Ratio ;
9. Surface He-3 Conc. (at g-1) ;
10. Surface He-3 Retention (%) ;

Rows within the “summary_mean_scenario_outputs” folder are file type “Mean Comparison File” and are named according to which group of scenarios they summarise; column names correspond to the erosion rates reported in the README for the individual files.
Row labels:
0: Mean Surface C-14 Conc. (at g-1) (Stochastic);
1: Mean Surface Be-10 Conc. (at g-1) (Stochastic)
2: Mean Surface C-14 / Be-10 Ratio (Stochastic);
3: Mean Surface He-3 Conc. (at g-1) (Stochastic); 
4. Mean Surfacef He-3 Retention (%) (Stochastic);
5. Mean 10Be-derived erosion rate (cm yr-1) (Stochastic);
6. Surface C-14 Conc. (at g-1) (Constant);
7. Surface Be-10 Conc. (at g-1) (Constant);
8. Surface C-14 / Be-10 Ratio (Constant);
9. Surface He-3 Conc. (at g-1) (Constant);
10. Surface He-3 Retention (%) (Constant);


All files follow the naming convention “EROSIONTYPE_distributiontype_cParetoshapevalue_filetype_EROSIONRATE.csv.” Example: STO_pareto_c0.8_comparison_output_ER0.129776384428187.csv. This indicates that the file is from a stochastic erosion scenario, which erodes according to a Pareto distribution with a shape value of 0.8, that it is a comparison_output type file (corresponding to a Scenario Comparison Output File in Table 1), and it has an erosion rate of 0. 129776384428187 cm yr-1. 
'''
