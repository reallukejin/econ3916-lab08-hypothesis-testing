# econ3916-lab08-hypothesis-testing
# Hypothesis Testing — Is Job Training Worth It?

## Objective
I tested whether the NSW job training program raised participants' 1978 earnings, and how big that effect was.

## Methodology
- Loaded the LaLonde NSW job training experiment (445 people: 185 trainees and 260 controls)
- Ran a one-sample t-test on control group earnings and a two-sample Welch's t-test comparing trainees to controls on 1978 earnings
- Wrote Welch's t-statistic as my own function, welch_t(), and checked it against scipy on the full sample and on five subgroups
- Computed Cohen's d to judge the size of the effect, not just whether it was significant
- Ran a power analysis to find the power of this study and the sample size needed to detect d = 0.3
- Tested the treatment effect in 5 overlapping demographic subgroups, then applied Bonferroni and Benjamini-Hochberg corrections
- Simulated p-value distributions when the null is true and when it is false

## Key Findings
- Trainees earned 1,794.34 dollars more in 1978 than controls (Welch's t = 2.6741, p = 0.0079), so the difference is statistically significant.
- The Cohen's d was 0.27, which is a small effect.
- 2 of the 5 subgroup effects were significant before correction, but only 1 was still significant after Bonferroni.
- Being significant doesn't by itself tell me the program is worth funding. That would also depend on costs and on whether the effect holds up in other groups.
