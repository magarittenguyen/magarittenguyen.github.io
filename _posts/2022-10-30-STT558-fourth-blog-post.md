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

After reading these artilces on model and variable selection, I've realized how much I don't know concerning regression models.  I'm left second guessing myself without concrete direction from a professor. Especially when these articles say "We recognize that true models do not exist. … A model will only reflect underlying patterns, and hence should not be confused with reality.". I exhibit some, if not most, of the downfalls mentioned in articles aimed at practicing statisticians with less experience. But, realizing one’s faults is not necessarily a bad thing. Being aware of what you are doing incorrectly can often be just as, or even more, useful than knowing your strengths.

Statistical models are useful tools applied in many research fields that connect an response/dependent variable to one or several independent variables (IVs) and quantifies the strength of associations between them. We also should recognize that no statistical model comes without assumptions. This sometimes introduces bias no matter how much we try to avoid it. 

Routine work for a practicing statisticain includes the development, estimation, and interpretation of statistical models for observational data geared towards answering research questions in life sciences -- this is most applicable to me as I work in drug development. 

Models mentioned in this field are as follows:  
- Predictive (or prognostic) models -- the aim to accurately predict an outcome value from a set of predictors  
- Explanatory models -- used in etiological research and should explain differences in outcome values by differences in explanatory variables  
- Descriptive models -- capture the association between dependent and independent variables

In the life sciences, models of all three types are needed. Still, they differ in the way they are used and interpreted.

Finally, as we recognize that no statistical model comes without any assumptions, we conclude that robustness to mild or moderate violations of those assumptions is also a key requirement.


.: How you would plan to determine variables to use in a regression model. :.





Variable selection is intended to select the best subset of predictors. But why bother?  
1. We want to explain the data in the simplest way redundant predictors should be removed. The principle of Occam's Razor states that among several plausible explanations for a phenomenon, the simplest is best. Applied to regression analysis, this implies that the smallest model that TS the data is best.   
2. Unnecessary predictors will add noise to the estimation of other quantities that we are interested in. Degrees of freedom will be wasted.  
3. Collinearity is caused by having too many variables trying to do the same job.  
4. Cost: if the model is to be used for prediction, we can save time and/or money by not measuring redundant predictors.  

Prior to variable selection:
1. Identify outliers and inuential points - maybe exclude them at least temporarily.  
2. Add in any transformations of the variables that seem appropriate.  

- we would need to know what type of data we are dealing with (my field is health sciences)  

- Many authors have repeatedly highlighted the importance of using background knowledge to guide variable selection. Background knowledge can be incorporated at least at two stages, and it requires an intensive interplay between the PI of the research project (usually a nonstatistician) and the statistician in charge of designing and performing statistical analysis. At the first stage, the PI will use subject‐specific knowledge to derive a list of IVs which in principle are relevant as predictors or adjustment variables for the study in question. This list will mostly be based on the availability of variables, and must not take into account the empirical association of IVs with the outcome variable in the data set.  

- I would either use all the varibles available -- the main effects, and the interaction effects (every interaction possible) -- ive only ever gone up to 3 varibles that have interactions... this is what I am familiar with  
- keep the lower order terms associated with the higher order terms... (e.g. if x^2, keep x)
	
.: What variable selection techniques do you prefer and why? :.  

-  again things from ST518 i cannot recall off the top of my head...  
-  cant seem to hide form EDA / EDA2...  
-  no analysis is bias-free, as all analysts factor their own bias into the equation  
-  there are a set of asusmptions we have to follow depending on the method we chose (all ST518)!!!  
-  i would either do forward or backwards selection and look at Tukey's Method (seems like this is the best method) ???  
-  if there is significance then i would keep the variable - if not, then i would remove it from the model...  
-  consider things that are too highly correlated and remove those  
-  run in sas using proc reg / prog glm to help out with this...  
-  what im most familiar with / most comfortable with I would use...  

- Hypothesis tests are the most popular criteria used for selecting variables in practical modeling problems.   
- forward selection (FS)   
- backward elimination (BE)  
- Backward elimination (BE)	 

    Start with the global model.  
    Repeat: Remove the most insignificant independent variable (IV) and reestimate the model.  
    Stop if no insignificant IV is left.  

	All (Wald) p‐values in multivariable model < αB  
	
- stepwise / stepwise regression (forward and backwards combines)
- 
- Criterion-based methods typically involve a wider search and compare models in a preferable manner. For this reason, I recommend that you use a
criterion-based method. -- AIC BIC
 
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
	
- In predictive research, variable selection may improve the accuracy of the predictions, but background knowledge can also be incorporated, going as far as updating the coefficients of an existing model with new data, and employing variable selection methods to assess that coefficients to update   

- now im ssecond guessing how i go about selecting varibales for my model because im not familiar with how my choices sould have a downfall  

e.g. from article below --> 5, 7, 8, 9  

I'm definitly in that group that does not have alot of experience... -_-  
 
- these articles are definitly informative, but im not sure i understood all of them 100%  


weaknesses:

1. For All-subset selection with more than 40 variables :     
	(a) The number of possible subsets can be huge.    
	(b) Often, there are several good models, although some are unstable.    
	(c) The best X variables may be no better than random variables, if the size sample is relatively smaller than the total number of variables.    
	(d) The regression statistics and regression coefficients are biased.   
2. All-subset selection regression can yield models that are too small.   
3. The rationale for the number of candidate variables, and not the number in the final model, is the number of degrees of freedom to consider.   
4. The data analyst knows more than the computer and failure to use that knowledge produces inadequate data analysis.    
5. Stepwise selection yields confidence limits that are far too narrow.   
6. Regarding the frequency of obtaining authentic predictor and noise variables, the degree of correlation among the predictor variables affects the frequency with which authentic predictor variables can fi nd their way into the final model. The number of candidate predictor variables can also affect the number of noise variables that gain entry to the model.    
7. Stepwise selection will not necessarily produce the best model if there are redundant predictors (a common problem).     
8. There are two distinct questions here: (a) When is Stepwise selection appropriate? and (b) Why is it so popular?   
9. As to question (b) above, there are two groups that are inclined to favor its usage. One consists of individuals, with little formal training in data analysis, who confuse knowledge of data analysis with knowledge of the syntax of SAS, SPSS and so on. They seem to feel that ‘ if it ’ s there in a program, it ’ s gotta be good – and
better than actually thinking about what my data might look like ’ . They are fairly easy to spot and condemn in a group of well-trained data analysts . However, there is also a second group that is often well trained. Its members believe in statistics, but believe that given any properly obtained database, a suitable computer program can objectively make substantive inferences without active consideration of the underlying hypotheses. Stepwise selection is the parent of this blind data analysis

EDA includes the following characteristics:   
1. Flexibility – techniques with greater flexibility to delve into the data;   
2. Practicality – advice on procedures to analyze data;  
3. Innovation – techniques for interpreting results;  
4. Universality – use all of statistics that apply to analyzing data; and  
5. Simplicity – above all, the belief that simplicity is the golden rule.  

(b) The Natural Seven-step Cycle of Statistical Modeling and Analysis  
1. Defi nition of the problem . Determining the best way to tackle the problem is not always obvious. Management objectives are often expressed qualitatively, in which case the selection of the outcome or target (dependent) variable is subjectively biased. When the objectives are clearly stated, the appropriate dependent variable is often unavailable, in which case a surrogate must be used.   
2. Determining technique . The technique fi rst selected is often that with which the data analyst is most comfortable, and not necessarily the best technique for solving the problem.   
3. Use of competing techniques . Applying alternative techniques increases the odds that a thorough analysis is conducted.   
4. Rough comparisons of effi cacy . Comparing the variability of results across techniques can suggest additional techniques or the deletion of alternative techniques.
5. Comparison in terms of a precise (and thereby inadequate) criterion . An explicit criterion is diffi cult to define;  therefore, precise surrogates are often used.
6. Optimization in terms of a precise and similarly inadequate criterion . An explicit criterion is diffi cult to define; therefore, precise surrogates are often used.
7. Comparison in terms of several optimization criteria . This constitutes the fi nal step in determining the best solution.  

CONCLUSION

Finding the best possible subset of variables to put in a model has been a frustrating exercise. Many variable selection methods exist. Many statisticians know them, but few know they produce poorly performing models. The resulting variable selection methods are a miscarriage of statistics because they are developed by debasing sound statistical theory to a misguided pseudotheoretical foundation. I have reviewed the five widely used variable selection methods, itemized some of their weaknesses, and described why they are used. I have then sought to present a better solution to variable selection in regression: the Natural Seven-step Cycle of Statistical Modeling and Analysis. I feel that newcomers to Tukey ’ s EDA need the Seven-step Cycle introduced within the narrative of Tukey ’ s analytic philosophy. Accordingly, I have embedded the solution within the context of EDA philosophy.  

Be alert to the danger that a model
contradictory to the tentative conclusions might be out there.

<!--
Your blog post can be written in a conversational tone or more formally (however you want to represent yourself).  There is no word count or anything like that, just make sure you answer the prompts above to receive full credit.

Submit the URL for your (rendered) github blog in the text box. 
-->
