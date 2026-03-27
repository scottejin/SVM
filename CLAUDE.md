# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the Notebook

Open and run `svm_wine_assignment.ipynb` in Jupyter:

```bash
jupyter notebook svm_wine_assignment.ipynb
# or
jupyter lab svm_wine_assignment.ipynb
```

Run all cells in order from top to bottom — later cells depend on variables set in earlier ones (e.g., `X_train_scaled`, `y_val`).

## Dependencies

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

## Project Structure

This is a single-notebook assignment. All code lives in `svm_wine_assignment.ipynb`.

**Data flow:**
1. `load_wine()` → `X` (13 features), `y` (3-class target)
2. `train_test_split` (70/30, stratified, `random_state=42`) → `X_train`, `X_val`
3. `StandardScaler` fit on train, applied to both splits → `X_train_scaled`, `X_val_scaled`
4. `SVC` models trained on scaled data

**Key variables available after Step 5:**
- `X_train_scaled`, `X_val_scaled`, `y_train`, `y_val` — used by all subsequent model cells
- `svm_linear`, `svm_rbf`, `y_pred_linear`, `y_pred_rbf` — from Steps 6–7

## Assignment Tasks (incomplete)

Tasks 1–5 and two bonus tasks need to be filled in. Each task has a placeholder markdown or code cell marked with `# Your answer goes here` or `<span style="color:red">Your answer goes here</span>`.
