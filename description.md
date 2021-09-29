<!--
*** This document is a thorough visualization of the donorschoose and stanford education data sets
-->




<!-- ABOUT THE PROJECT -->
# DonorsChoose Dataset

## School Distributuion


![Continental](https://github.com/zyuan-mkt/Education-Project/blob/main/figures/distribution.png)
![Alaska](https://github.com/zyuan-mkt/Education-Project/blob/main/figures/HI.png)
![Hawaii](https://github.com/zyuan-mkt/Education-Project/blob/main/figures/AK.png)
![Hist](https://github.com/zyuan-mkt/Education-Project/blob/main/figures/school_distribution.png)



## Project Description
### Variation by Year

![Year](./figures/num_year.png)
![Price](./figures/proj_price.png)

![Grade Level](./figures/grade_level.png)
![Focus Level](./figures/pri_focus.png)
![Resource Type](./figures/res_typ.png)
![Metro Level](./figures/met_typ.png)
![Poverty Level](./figures/pov_level.png)

![Focus Level Length](./figures/foc_level_len.png)
![Poverty Level Length](./figures/pov_level_len.png)
![Metro Level Lenghth](./figures/met_level_len.png)
![Grade Level Lenghth](./figures/grd_level_len.png)
![Resource Type Length](./figures/res_typ_len.png)


### Variation by Teacher Prefix

![Year](./figures/gender.png)

![Grade Level](./figures/pre_grd.png)
![Focus Level](./figures/pre_focus.png)
![Resource Type](./figures/pre_res.png)
![Metro Level](./figures/pre_met.png)
![Poverty Level](./figures/pre_pov.png)

![Focus Level Length](./figures/pre_foc_sent.png)
![Poverty Level Length](./figures/pre_pov_sent.png)
![Metro Level Lenghth](./figures/pre_met_sent.png)
![Grade Level Lenghth](./figures/pre_grd_sent.png)
![Resource Type Length](./figures/pre_res_sent.png)

### Variation in Writing

![Grade Level](./figures/wri_grd.png)
![Focus Level](./figures/wri_foc.png)
![Resource Type](./figures/wri_res.png)
![Metro Level](./figures/wri_met.png)
![Poverty Level](./figures/wri_pov.png)
![Teacher Prefix](./figures/wri_pre.png)

### Variation in Stanford Education Data
School Covariates
* sch_sped	special education school indicator flag (CRDC) (2018)	
* totenrl	total enrollment (CCD) (2009-18 weighted average)	
* perwht	proportion white (CCD) (2009-18 weighted average)	
* pernam	proportion native american (CCD) (2009-18 weighted average)	
* perasn	proportion asian (CCD) (2009-18 weighted average)	
* perhsp	proportion hispanic (CCD) (2009-18 weighted average)	
* perblk	proportion black (CCD) (2009-18 weighted average)	
* perfl	proportion free lunch eligible (CCD) (2009-18 weighted average)	
* perrl	proportion reduced lunch eligible (CCD) (2009-18 weighted average)	
* perfrl	proportion free or reduced lunch eligible (CCD) (2009-18 weighted average)	
* perecd	proportion economically disadvantaged (Ed Facts) (2009-18 weighted average)	
* gifted_tot	proportion classified as gifted (CRDC) (2012, 2014, 2016, 2018 weighted average)	
* disab_tot	proportion classified as disabled (CRDC) (2012, 2014, 2016, 2018 weighted average)	
* disab_tot_id	proportion classified as disabled (IDEA Only) (CRDC) (2012, 2014, 2016, 2018 weighted average)	
* lep	proportion limited english proficient (CRDC) (2012, 2014, 2016, 2018 weighted average)	
* gifted_flag	school has 40%+ gifted students	
* lep_flag	school has 50%+ LEP students	
* sped_flag	school has 40%+ special education students or is listed as a special education school in CCD or CRDC	
* spedidea_fla	school has 40%+ sped students (IDEA only) OR is listed as sped school in CCD or CRDC	
* avgrdall	average per grade enrollment (CCD) (2009-18 weighted average)

![School Covariates](./figures/cor_sch.png)
Academic Achievements
* gradecenter	Grade used for pooled centering	
* gap	Gap Estimate Indicator	
* tot_asmts	Total number of math + RLA tests for pooled estimates	
* cellcount	Total number of math + RLA cells for pooled estimates	
* mn_asmts	Per grade number of math + RLA cells for pooled estimates (tot_asmts/cellcount)	
* cs_mn_avg_ol	School Mean Ach, Math&RLA, OLS est, CS		School Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Ordinary Least Squares (OLS) estimate,  Cohort Scale (CS)	* 
* cs_mn_coh_ol	School Cohort Slope of Mean Ach, Math&RLA, OLS est, CS		School Cohort Slope of Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Ordinary Least Squares (OLS) estimate,  Cohort Scale (CS)	
* cs_mn_grd_ol	School Grade Slope of Mean Ach, Math&RLA, OLS est, CS		School Grade Slope of Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Ordinary Least Squares (OLS) estimate,  Cohort Scale (CS)	
* cs_mn_mth_ol	School Math-RLA Diff in Mean Ach, Math&RLA, OLS est, CS		School Math-RLA Diff in Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Ordinary Least Squares (OLS) estimate,  Cohort Scale (CS)	
* cs_mn_avg_eb	School Mean Ach, Math&RLA, EB est, CS		School Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Empirical Bayes (EB) estimate,  Cohort Scale (CS)	
* cs_mn_coh_eb	School Cohort Slope of Mean Ach, Math&RLA, EB est, CS		School Cohort Slope of Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Empirical Bayes (EB) estimate,  Cohort Scale (CS)	
* cs_mn_grd_eb	School Grade Slope of Mean Ach, Math&RLA, EB est, CS		School Grade Slope of Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Empirical Bayes (EB) estimate,  Cohort Scale (CS)	
* cs_mn_mth_eb	School Math-RLA Diff in Mean Ach, Math&RLA, EB est, CS		School Math-RLA Diff in Mean SEDA EDFacts Test-Based Achievement  Math&RLA, Empirical Bayes (EB) estimate,  Cohort Scale (CS)H40	
![Academic Achievements](./figures/cor_ach.png)

