# Do Coup Attempts Beget Coups? *A causal analysis with V-Dem*

*Author: Troy Cheng, Hongzhe Wang*

---

## Research question
**RQ.** Do coup attempts in year _t_ increase the probability that the regime ends **via a coup** in year _t+1_?

- **Treatment (A_t):** `e_pt_coup_attempts > 0` in year _t_.  
- **Outcome (Y*_{t+1}):** from `v2regendtype` in _t+1_; coded **1** for {military coup, non-military coup, self-coup} and **0** for all other non-missing codes, including “still exists”.

## Design
We estimate within-country contrasts by absorbing **country** and **year** effects and adding a time-varying confounder (**civil war**, `e_civil_war`). Models: (i) FE logit (country & year FE, clustered SEs); (ii) mixed-effects logit (country random intercept + year FE); (iii) (ii) + civil war. We report odds ratios and g-computed average risk differences.

## Results
All specifications yield OR ≈ **0.7** for `attempt` and an average risk difference ≈ **−0.02** to **−0.024**. Unadjusted splits look positive, but the association vanishes (and slightly flips) once we compare **within countries over time**.

**One-sentence takeaway:** After aligning time and adjusting for country/year structure (and civil war), **coup attempts in year _t_ do not raise the chance that the regime ends via a coup in _t+1_**; the g-computed risk difference is about **−2–3 pp**.

