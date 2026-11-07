# Statistical Analysis Projects

Two data analysis projects in Python: a hypothesis test on FIFA World Cup goals and an exploratory analysis of crime patterns in Los Angeles. Both started as DataCamp projects and are documented here with my own code and analysis.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![pingouin](https://img.shields.io/badge/pingouin-4C72B0)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

## 1. Do women's World Cup matches score more goals?

[`notebooks/01_world_cup_goals_hypothesis_test.ipynb`](notebooks/01_world_cup_goals_hypothesis_test.ipynb)

- **Data:** 584 official FIFA World Cup matches since 2002 (384 men's, 200 women's).
- **Method:** the goal counts are right-skewed and not normal, so I used a one-sided **Mann-Whitney U test** instead of a t-test, with a significance level of 10%.
- **Result:** p-value = 0.005, so the null hypothesis is rejected. Women's World Cup matches score significantly more goals than men's (2.98 vs 2.51 goals per match on average).

## 2. Crime patterns in Los Angeles

[`notebooks/02_la_crime_patterns.ipynb`](notebooks/02_la_crime_patterns.ipynb)

Analysis of **185,715** LAPD crime records to help allocate police resources:

| Question | Answer |
|---|---|
| Hour with the most crimes | **12:00** (noon) |
| Area with the most night-time crimes (10 pm to 3:59 am) | **Central** |
| Most affected victim age group | **26–34** (47,470 crimes) |

## Run it

```bash
git clone https://github.com/said-velasquez/statistical-analysis-projects.git
cd statistical-analysis-projects
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Download the data first and put it in `data/` (see [`data/README.md`](data/README.md)).

## Tech stack

Python, pandas, NumPy, pingouin, Matplotlib, Seaborn, Jupyter.

## Author

**Said Velásquez**, Computer Engineering student based in Madrid.
[LinkedIn](https://www.linkedin.com/in/said-vel%C3%A1squez-650905333) · [GitHub](https://github.com/said-velasquez)
