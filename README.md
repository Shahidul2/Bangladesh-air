# GraphSurrogate-ADR (GS-ADR): Physics-Informed Forecasting in Bangladsesh

This project introduces **GraphSurrogate-ADR (GS-ADR)**, a physics-informed graph neural network for multi-horizon fine particulate matter forecasting across 29 cities in Bangladesh. 
The model integrates a discretized advection-diffusion-reaction (ADR) backbone with graph-aware neural source terms to ensure mechanistically legible predictions.

#### Core Models:

* **GS-ADR (Proposed):** Physics-informed NN with graph Laplacian diffusion and decay.
* **Baselines:** Persistence, LSTM, Vector Autoregression (VAR), HistGBR, and Seasonal Naïve.

#### Key Features:

* **Physics-Informed Constraints:** Enforces mass-consistency and non-negativity via soft inequality penalties.
* **Hybrid Uncertainty Quantification:** Combines aleatoric (heteroscedastic regression) and epistemic (Monte Carlo dropout) uncertainty for calibrated risk assessment.
* **Decision-Ready Early Warning:** Implements tiered alerting thresholds at Advisory and Emergency operating points.

#### Evaluation Metrics:

* **Point Accuracy:** MAE, RMSE, 
* **Episode Resilience:** Extreme RMSE (top 10% events)
* **Plausibility:** Violation Rate (%) and Violation Magnitude
* **Probabilistic Skill:** Brier Score, Expected Calibration Error (ECE), AUPRC

### Repository Contents:

* `Images/`: Diagnostic visualizations including network geography (Fig. A1), city chemistry fingerprints (Fig. A2), and seasonal diurnal cycles (Fig. A4).
* `Code/`: Implementation of the ADR-inspired graph update and the UQ decision layer.
* `Data/`: Data utilized in the study (2023-2025), 29 Cities in Bangladesh.
