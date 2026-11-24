> **Deprecated:** This notebook's error and error-free scenarios were labeled based on HTTP status codes. This approach is not suitable for determining whether an application or Kubernetes deployment has actually got errors.

For example, a user entering incorrect login credentials may receive an HTTP 401 response. Although this is an expected authentication outcome, status-code-based labeling can classify it as an error. Therefore, the notebook's test was limited to HTTP status-code classification and should not be treated as a reliable test of application or deployment failure prediction.

> **Dataset note:** The Random Forest and XGBoost models in this notebook were trained and tested on our old dataset, **not** on the classified/labeled [Baseline-Dataset-phase-3](https://github.com/USJ-Research/Baseline-Dataset-phase-3) dataset. The old dataset has since been deleted, so these results can't be reproduced.
