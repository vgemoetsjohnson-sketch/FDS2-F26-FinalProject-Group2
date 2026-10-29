# fds2-F26-finalproject-group2
# Names: Victoria Gemoets-Johnson, Elijah Gilbert, Anna Havner
<<<<<<< HEAD

Team 2
- Anna (GitHub: @annahavner-byte) owns proposal.ipynb

- Victoria (GitHub: @vgemoetsjohnson-sketch) . owns 00_load_data.ipynb

- Elijah (GitHub: @elgilbert-star)

it


# Project Proposal

by: Victoria Gemoets-Johnson, Elijah Gilbert, Anna Havner

import pandas as pd

pvd = pd.read_excel('data/pvdstudy.xlsx')
pvd

hrsn = pd.read_csv('data/hrsnstudy.csv')
hrsn

# Data Summary

We are working with two data sets, one that focuses on hypertension and postpartum and one that centers on disease aversion and pregnancy. We found these public data sets on the provided OSF website. The "Disease Aversion and Pregnancy" data set (PVD), was collected by The "Hypertension and Postpartum" data set (HRSN), was collected by

Each row represents on individual person. The variables we are planning to use out of the PVD data set are The variables we are planning to use out of the HRSN data set are




# Question 3
Victoria - How does age impact the relationship between socioeconomic status and the health of an individual?

import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

pvd_cols = ['Age','Education','Income','SES self-assessment (1very poor to 7very good)','Number of health problems during pregnancy (max 22)','Disease severity 0to7','SUM (0-40)',]

pvd = pvd.rename(columns={
    'Income (1 - below 600, 2 - 600 - 1000, 3- 1000 - 1500, 4 - 1500 - 2000, 5 - 2000 - 3000, 6 - 3000 - 4000, 7 - 4000 - 6000, 8 - over 6000 PLN)': 'Income'})

hrsn_cols = ['age', 'insurance', 'count_total_need_plus_tp2', 'ed_or_hosp', 'pcp', 'pp_visit_6_wks']

# correlation
pvd_cols = pvd[pvd_cols].apply(pd.to_numeric, errors='coerce')
pvd_corr = pvd_cols.corr()

hrsn_cols = hrsn[hrsn_cols].apply(pd.to_numeric, errors='coerce')
hrsn_corr = hrsn_cols.corr()

# heat map
fig, axes = plt.subplots(1, 2, figsize=(15, 6), gridspec_kw={'width_ratios': [7, 6]})
for ax, corr, title in zip(axes, [pvd_corr, hrsn_corr], ['pvd (pregnancy study)', 'hrsn (postpartum study)']):
    sns.heatmap(corr, annot=True, fmt='.2f', cmap='coolwarm', vmin=-1, vmax=1, ax=ax, cbar=False)
    ax.set_title(title)
fig.colorbar(axes[1].collections[0], ax=axes, label='Pearson correlation', shrink=0.8)
fig.suptitle('Age, SES and health in both datasets', fontweight='bold')
plt.show()


My plan: my overall plan is to examine how age shapes the relationship between socioeconomic status and health, using both of the two datasets from above. The plan is to clean the data by keeping the columns that matter to do those calculations and observations along with dropping rows only where needed, then to combine education, income and self-rated SES into a single index for pvd and use social needs and insurance as the SES measures for hrsn.

For now, heat maps will give an overview of how age, SES and health outcomes relate. Then I will use scatter plots and bar charts split by age group to show whether the SES-health link looks different for younger and older participants which I will make a score for age group to do this as well.

Expected outcomes: I expect lower SES to be associated with worse health and more health-care strain in both datasets, and I hypothesize that the association will differ by age, mainly the older you are the worse SES status will impat your age. Because the samples are kinda small I expect some results to be suggestive rather than very clear of this prediction.

