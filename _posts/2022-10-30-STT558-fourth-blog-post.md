## ST558 - My Fourth Blog Post  

<!--
Overview

This assignment is to create a blog post using your github blog.  See below for the blog post prompt. Assesses LO 1.3 and others.
Completion time

The estimated time to complete this assignment is 20-40 minutes.
-->

### Instructions  
#### Write a blog post to respond to the prompt below:

#### When building regression models, it often takes a lot of experience and knowledge about your data in order to determine the variables and transformation of variables that you want to include in the model building process.  There are many variable selection techniques (or feature selection) but it can be a confusing practice when you are first learning.  Read through these articles (and others if you'd like to find your own):  

> https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5969114/  
> https://www.biostat.jhsph.edu/~iruczins/teaching/jf/ch10.pdf  
> https://link.springer.com/content/pdf/10.1057/jt.2009.26.pdf   

For your blog post, write up a brief discussion of how you would plan to determine variables to use in a regression model.  What variable selection techniques do you prefer and why?.  

<!--
https://quantifyinghealth.com/variables-to-include-in-regression/
-->


Statistical models are useful tools applied in many research fields dealing with empirical data. They connect an outcome variable to one or several so‐called independent variables and quantify the strength of association between IVs and outcome variable.

“We recognize that true models do not exist. … A model will only reflect underlying patterns, and hence should not be confused with reality.”

Finally, as we recognize that no statistical model comes without any assumptions, we conclude that robustness to mild or moderate violations of those assumptions is also a key requirement.

This is because most of the methods that are described and discussed here were developed for the linear model with Gaussian errors, but were then transferred to other models for noncontinuous outcome variables.

The paper is intended for the practicing statistician, whose routine work includes the development, estimation, and interpretation of statistical models for observational data to help answering research questions in life sciences. (most applicable to me)

Within predictive research questions, predictive (or prognostic) models have the aim to accurately predict an outcome value from a set of predictors. Explanatory models are used in etiological research and should explain differences in outcome values by differences in explanatory variables. Finally, descriptive models should “capture the association between dependent and independent variables” (Shmueli, 2010). In the life sciences, models of all three types are needed. Still, they differ in the way they are used and interpreted.

While prognostic models focus on predictions, explanatory models are used to estimate (causal) effects of risk factors or exposures by means of adjusted effect estimation, and descriptive models can have elements of both.

The purpose of statistical modeling in a particular analysis will have impact on the selection of IVs for a model

Common assumptions of these models are linearity, that is the expected outcome value is thought to be modeled by a linear combination of IVs, and additivity, that is the effects of the IVs can be added. 



.: How you would plan to determine variables to use in a regression model. :.

- we would need to know what type of data we are dealing with (my field is health sciences)

- Many authors have repeatedly highlighted the importance of using background knowledge to guide variable selection. Background knowledge can be incorporated at least at two stages, and it requires an intensive interplay between the PI of the research project (usually a nonstatistician) and the statistician in charge of designing and performing statistical analysis. At the first stage, the PI will use subject‐specific knowledge to derive a list of IVs which in principle are relevant as predictors or adjustment variables for the study in question. This list will mostly be based on the availability of variables, and must not take into account the empirical association of IVs with the outcome variable in the data set.

	
.: What variable selection techniques do you prefer and why? :.



- Hypothesis tests are the most popular criteria used for selecting variables in practical modeling problems. 
- forward selection (FS) 
- backward elimination (BE)
- Backward elimination (BE)	

    Start with the global model.
    Repeat: Remove the most insignificant independent variable (IV) and reestimate the model.
    Stop if no insignificant IV is left.

	All (Wald) p‐values in multivariable model < αB
 
- The Akaike information criterion (AIC) 
- The Bayesian information criterion (BIC) was developed for situations where one assumes existence of a true model that is in the scope of all models that are considered in model selection.

- Situation	
For some IVs it is known from previous studies that their effects are strong, for example age in cardiovascular risk studies or tumor stage at diagnosis in cancer studies.	
- Recommendation
Do not perform variable selection on IVs with known strong effects.

- Often one is willing to trade in a little bias in return for considerably reduced variance. This means, that even in explanatory models where the set of adjustment variables necessary to control confounding is assumed to be known, some of the confounders’ association with the outcome may be so weak that adjustment may increase variance in the effect estimate of main interest more than reducing its bias. Consequently, depending on whether the true association of a potential confounder with the outcome is weak or strong, variable selection may be beneficial or harmful, even if performed with the same significance criterion. 

- (i) if background knowledge on the strength of a confounder exists, it should be used to decide whether variable selection should be applied or not, and (ii) one cannot recommend a universally applicable significance criterion for variable selection that fits all needs.

- 

	SAS procedures
	Modeling techniques	PROC GLMSELECT	PROC REG	PROC LOGISTIC 
	

<!--
Your blog post can be written in a conversational tone or more formally (however you want to represent yourself).  There is no word count or anything like that, just make sure you answer the prompts above to receive full credit.

Submit the URL for your (rendered) github blog in the text box. 
-->
