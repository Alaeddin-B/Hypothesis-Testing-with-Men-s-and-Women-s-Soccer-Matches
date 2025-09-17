# Hypothesis Testing: Men's vs. Women's FIFA World Cup Goals

This project investigates whether more goals are scored in women's international soccer matches than men's, using official FIFA World Cup match data since 2002.

## Project Overview

- **Goal:** Test the hypothesis that the mean number of goals in women's matches is greater than in men's.
- **Data:**
  - `men_results.csv`: Results of men's international matches
  - `women_results.csv`: Results of women's international matches
- **Analysis:**
  - Data filtered for FIFA World Cup matches since 2002-01-01
  - Total goals per match calculated
  - One-sided independent t-test performed
  - 10% significance level ($\alpha = 0.10$)

## Files

- `notebook.ipynb`: Main analysis notebook
- `men_results.csv`, `women_results.csv`: Data files
- `soccer-pitch.jpg`: Project illustration
- `requirements.txt`: Python dependencies

## How to Run

1. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Open `notebook.ipynb` in Jupyter or VS Code.
3. Run all cells to reproduce the analysis.

## Methodology

- Data is loaded and filtered for relevant matches.
- Total goals per match are computed.
- An independent t-test (one-sided, alternative="greater") compares the means.
- The p-value and test result are stored in a dictionary:

  ```python
  result_dict = {"p_val": p_val, "result": result}
  ```

  where `result` is "reject" or "fail to reject" the null hypothesis.

## Interpretation

- If the p-value is less than 0.10, we reject the null hypothesis and conclude that more goals are scored in women's matches.
- Otherwise, we fail to reject the null hypothesis.

## License

This project is for educational purposes.
