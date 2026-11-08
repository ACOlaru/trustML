# TrustML

**An open-source Python toolkit for evaluating the reliability of machine learning models.**

TrustML is a project focused on an important question in machine learning: how much should we trust a model's predictions?

A model can achieve high accuracy and still produce poorly calibrated probabilities, behave unpredictably when data changes, or make mistakes with high confidence. TrustML aims to make these issues easier to measure through practical evaluation tools, statistical analysis, and reproducible experiments.

The project is actively under development.

## What it does

TrustML provides tools to evaluate several aspects of model reliability:

- **Model performance:** Measure prediction accuracy.
- **Probability calibration:** Evaluate how closely predicted confidence matches actual correctness using Expected Calibration Error (ECE) and Brier score.
- **Uncertainty estimation:** Calculate predictive entropy and margin-based uncertainty.
- **Selective prediction:** Measure model risk at different prediction coverage levels.
- **Distribution shift:** Compare model performance under changed data and detect feature-level distribution changes.
- **Reliability reporting:** Combine multiple evaluation metrics into a single report.

## Experiments

The project includes experiments comparing machine learning models and calibration techniques.

Current work includes:

- Comparing logistic regression and random forest models.
- Evaluating sigmoid and isotonic probability calibration.
- Testing models across different datasets.
- Measuring accuracy, ECE, Brier score, and log loss.
- Using bootstrap confidence intervals and paired comparisons to assess results.
- Investigating how models behave under changes in data distributions.

The goal is to understand not just which model performs best, but also how reliable its predictions are.

## Tech stack

- Python
- NumPy
- SciPy
- scikit-learn
- Matplotlib
- pytest
- Git

## Project structure

```text
trustML/
├── src/
│   ├── trustml/
│   │   ├── data.py
│   │   ├── calibration.py
│   │   ├── uncertainty.py
│   │   ├── selective.py
│   │   ├── shift.py
│   │   ├── shift_detection.py
│   │   └── report.py
│   └── experiments/
├── tests/
├── reports/
├── pyproject.toml
└── README.md
```

## Getting started

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/trustML.git
cd trustML
```

Create a virtual environment:

```bash
python -m venv .venv
```

Install the project and development dependencies:

```bash
python -m pip install -e ".[dev]"
```

Run the tests:

```bash
python -m pytest tests/ -v
```

Run an experiment:

```bash
python src/experiments/benchmark.py
```

## Development goals

TrustML is being developed as a practical reliability evaluation toolkit, with an emphasis on correctness, reproducibility, and clear engineering.

Planned improvements include:

- More robust evaluation across different datasets.
- Additional calibration and uncertainty metrics.
- Better statistical comparisons between models.
- More comprehensive test coverage.
- Improved reporting and visualisation.
- Documentation and examples for using the toolkit.

## License

MIT License.

## Author

An independently developed open-source project focused on Python software engineering, machine learning evaluation, and statistical reliability.
