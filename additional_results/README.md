# Additional Results

Here we provide an extended set of results to supplement those presented in the paper. In particular, we show results on additional downstream tasks using the EchoNetLVH model, and include the uniform random sampling strategy as an additional baseline. It is clear in the figure below that the task-based information gain strategy outperforms baselines across each of the EchoNetLVH measurement tasks. To reproduce these results, first run the benchmarking script `benchmarking_scripts/eval_downstream_task_echonetlvh.py`, and then generate the plot below using `plotting/plot_downstream_task_results.py`.


<img width="2109" height="770" alt="combined_measurement_mae" src="https://github.com/user-attachments/assets/d2776765-0464-4880-81ba-2233f90fb98e" />

## MAE Statistics (Mean ± Std) by Strategy and Measurement Type

### LVPW MAE [cm]

| Strategy | 1/256 Scan Lines | 3/256 Scan Lines | 5/256 Scan Lines |
|---|---|---|---|
| Task-Based Information Gain | **0.087 ± 0.030** | **0.054 ± 0.021** | **0.044 ± 0.021** |
| General Information Gain | 0.116 ± 0.039 | 0.081 ± 0.025 | 0.066 ± 0.020 |
| Uniform Random | 0.125 ± 0.038 | 0.081 ± 0.029 | 0.064 ± 0.023 |

### LVID MAE [cm]

| Strategy | 1/256 Scan Lines | 3/256 Scan Lines | 5/256 Scan Lines |
|---|---|---|---|
| Task-Based Information Gain | **0.292 ± 0.139** | **0.169 ± 0.095** | **0.132 ± 0.078** |
| General Information Gain | 0.440 ± 0.155 | 0.281 ± 0.114 | 0.220 ± 0.086 |
| Uniform Random | 0.537 ± 0.197 | 0.293 ± 0.110 | 0.211 ± 0.090 |

### IVS MAE [cm]

| Strategy | 1/256 Scan Lines | 3/256 Scan Lines | 5/256 Scan Lines |
|---|---|---|---|
| Task-Based Information Gain | **0.129 ± 0.056** | **0.078 ± 0.041** | **0.064 ± 0.038** |
| General Information Gain | 0.190 ± 0.060 | 0.117 ± 0.052 | 0.093 ± 0.044 |
| Uniform Random | 0.227 ± 0.069 | 0.125 ± 0.047 | 0.092 ± 0.040 |
