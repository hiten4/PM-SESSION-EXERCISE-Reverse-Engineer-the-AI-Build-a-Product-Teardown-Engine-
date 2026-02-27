# Reflection Responses

## 1️ Which of the 6 layers surprised you the most in terms of complexity for PhonePe’s fraud detection? Why?

Layer 1 — **Data Foundation** was the most surprisingly complex. Fraud detection is often thought of as a modeling problem, but the real difficulty lies in computing high-cardinality, low-latency velocity and graph features consistently across streaming and training environments. The need to maintain strict online–offline feature parity under massive transaction throughput makes this layer more engineering-heavy than the model itself. A small inconsistency in feature computation can silently degrade model performance at scale.

---

## 2️ What was the single biggest difference you noticed between the LLMs you tested?

The biggest difference wasn’t fluency — it was **system-level reasoning depth**. One model could describe components (e.g., “use XGBoost for fraud detection”), while another structured the architecture into multi-stage pipelines (rule engine → ML scorer → graph propagation → calibrated decisioning) and justified trade-offs like latency vs recall. The stronger model explicitly reasoned about adversarial drift, class imbalance metrics (PR-AUC vs ROC), and deployment constraints, rather than stopping at algorithm selection. That ability to think in production constraints — not just model types — was the key differentiator.
