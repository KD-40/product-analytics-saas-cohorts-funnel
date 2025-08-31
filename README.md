
Product Analytics: Cohorts & Funnel
Overview
Cohort retention analysis (Day 2) with a saved heatmap and reproducible notebook; funnel analysis planned next.

Repo structure
assets/: figures (e.g., retention_heatmap_v0.png)

data/: CSV exports from SQL Developer (UTF‑8, Comma, Header)

notebooks/: Jupyter notebooks (e.g., retention_analysis.ipynb)

reports/: memos with findings and actions

sql/: SQL used to build matrices/funnels

Day 2: reproduce steps
Export cohort results from SQL Developer grid: right‑click → Export → Format=CSV, Encoding=UTF‑8, Separator=Comma, Include Header=Yes → save to data/retention_matrix.csv.

Open notebooks/retention_analysis.ipynb in VS Code (recommend setting Jupyter “Notebook File Root” to ).

Run cells to load CSV, pivot to a retention matrix, and save the heatmap image to assets/retention_heatmap_v0.png.

Notes
Line endings on Windows: configure Git once with git config --global core.autocrlf true or add a .gitattributes policy for consistency.

Keep large raw exports out of GitHub or use LFS as needed.

Next (Day 3)
Build a funnel (signup → verify_email → onboard_completed → start_trial → upgrade), segment by acquisition_channel and device_type, export via SQL Developer CSV, then analyze conversion and drop‑offs in a new notebook.
