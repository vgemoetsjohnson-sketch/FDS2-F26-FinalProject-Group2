# fds2-F26-finalproject-group2
# Names: Victoria Gemoets-Johnson, Elijah Gilbert, Anna Havner
<<<<<<< HEAD

Team 2
- Anna (GitHub: @annahavner-byte) owns proposal.ipynb

- Victoria (GitHub: @vgemoetsjohnson-sketch) . owns 00_load_data.ipynb

- Elijah (GitHub: @elgilbert-star)



# Project Proposal

by: Victoria Gemoets-Johnson, Elijah Gilbert, Anna Havner

Perceived Vulnerability to Disease: https://osf.io/7fjd6/files/5c84q

Hypertension and Postpartum: https://osf.io/hq7vg/files/bcgwt

# Data Summary

We are working with two data sets, one that focuses on hypertension and postpartum and one that centers on disease aversion and pregnancy. We found these public data sets on the provided OSF website. The "Disease Aversion and Pregnancy" data set (PVD), was collected by The "Hypertension and Postpartum" data set (HRSN), was collected by

Each row represents on individual person. The variables we are planning to use out of the PVD data set are The variables we are planning to use out of the HRSN data set are

# Question 1
Anna - Does a mother’s pre-existing physiological or psychological burden compound the negative impacts of pregnancy-related complications on newborn health?

Plan: My overall plan is to examine the Perceived Vulnerability to Disease dataset to explore how extra physiological stress has adverse effects in pregnancy-related complications. I plan to use the columns noting prenatal physiological health in the individuals (Allergies, Asthma, Endometriosis, Diabetes, Hypertension, Thyroid problems, Hormonal Problems) to make a physiological health burden index, and use the columns noting prenatal psychological health (Perceived Stress Scale, Germ Aversion Sum, Infectability sum) to make a psychological health burden index. I will look into individual effects in newborn health (APGAR score, birth weight) but I will create an overall newborn health index to use for general comparisons.. I will then look at pregnancy-related complications (Pregnancy diabetes 1Y, Thyroid gland problems 1Y, Hypertension 1Y) with newborn health outcomes and compare differences among subsets of individuals with better or worse prenatal health.

Expected Outcomes: I expect to see that individuals with worse prenatal health, both physiological and psychological, have compounded adverse health effects during pregnancy on newborn health outcomes. One possible limitation is in examining psychological health, I don't have very much data on this. If I could find a similar dataset that also included anxiety, depression, etc. it could be better to examine the psychological aspect with. In making this first look, I have also discovered that a big limitation is inconsistency of data within my dataset. It is very unlikely that only one individual in this study had asthma, yet in the first plot I made, only one datapoint shows Yes to having had asthma.

# Question 2
Elijah - Which life circumstances best predict pregnant women's stress: economic status, relationship stability, or whether the pregnancy was planned?

Exploratory Findings (First-Look Boxplots)
Unplanned pregnancies exhibit noticeably higher median stress scores compared to planned pregnancies.
Lower income tiers show elevated median stress scores relative to middle and high income groups.
Unmarried participants display slightly higher median stress scores than married participants.
3. Analysis Plan & Next Steps
Multiple Regression Analysis: To determine which life circumstance is the primary independent driver of stress, we will fit a multiple linear regression combining financial status, pregnancy planning, and relationship status. This will isolate the effect of each factor while controlling for the others.
Step Beyond FDS I: We plan to implement a train/test split (held-out data evaluation) to assess how accurately a model trained on these baseline life circumstances can predict high vs. low maternal stress levels on unseen data.
4. Expected Outcomes
If Hunch is Supported: Financial status / lower income will demonstrate the largest standardized effect (
) on stress scores when holding pregnancy planning and marital status constant.
If Hunch is Wrong: Pregnancy planning status or marital status will retain a larger significant association with stress scores than income once all variables are evaluated together in the multiple regression model.


# Question 3
Victoria - How does age impact the relationship between socioeconomic status and the health of an individual?

My plan: my overall plan is to examine how age shapes the relationship between socioeconomic status and health, using both of the two datasets from above. The plan is to clean the data by keeping the columns that matter to do those calculations and observations along with dropping rows only where needed, then to combine education, income and self-rated SES into a single index for pvd and use social needs and insurance as the SES measures for hrsn. For now, heat maps will give an overview of how age, SES and health outcomes relate. Then I will use scatter plots and bar charts split by age group to show whether the SES-health link looks different for younger and older participants which I will make a score for age group to do this as well.

Expected outcomes: I expect lower SES to be associated with worse health and more health-care strain in both datasets, and I hypothesize that the association will differ by age, mainly the older you are the worse SES status will impat your age. Because the samples are kinda small I expect some results to be suggestive rather than very clear of this prediction.

