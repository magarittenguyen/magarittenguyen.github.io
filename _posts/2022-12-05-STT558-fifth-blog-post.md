## ST558 - My Fifth Blog Post  

<!--
Overview

This assignment is to create a blog post using your github blog.  See below for the blog post prompt. Assesses LO 1.3 and others.
Completion time

The estimated time to complete this assignment is 20-40 minutes.
-->



 
    We're just about done with the course (woot)! 
        What things are you going to do differently in practice now that you've had this course?
        Data science (and statistics) is a huge field. What do you hope to do in relation to data science (and statistics) in your future career? What aspects/areas do you want to learn more about? 

    Your blog post can be written in a conversational tone or more formally (however you want to represent yourself).  There is no word count or anything like that, just make sure you answer the prompts above to receive full credit.
    Submit the URL for your (rendered) github blog post in the text box. 
    
### Instructions  
#### Write a blog post to respond to the prompt below:

#### When building regression models, it often takes a lot of experience and knowledge about your data in order to determine the variables and transformation of variables that you want to include in the model building process.  There are many variable selection techniques (or feature selection) but it can be a confusing practice when you are first learning.  Read through these articles (and others if you'd like to find your own):  

> https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5969114/  
> https://www.biostat.jhsph.edu/~iruczins/teaching/jf/ch10.pdf  
> https://link.springer.com/content/pdf/10.1057/jt.2009.26.pdf   

For your blog post, write up a brief discussion of how you would plan to determine variables to use in a regression model.  What variable selection techniques do you prefer and why?  

<!--
https://quantifyinghealth.com/variables-to-include-in-regression/
-->

After reading these articles on model and variable selection, I've realized how much I don't know concerning regression models.  I'm left second guessing myself without concrete direction from a professor. Especially when these articles say "We recognize that true models do not exist. … A model will only reflect underlying patterns, and hence should not be confused with reality.". I exhibit some, if not most, of the downfalls mentioned in articles aimed at practicing statisticians with less experience. But, realizing one’s faults is not necessarily a bad thing. Being aware of what you are doing incorrectly can often be just as, or even more, useful than knowing your strengths. A lot of this was learned in ST518, but I'm having trouble recalling because I don't use this in my daily life. These articles are definitely informative, but I'm not sure I understood all of them 100%.  

Statistical models are useful tools applied in many research fields that connect a response/dependent variable to one or several independent variables (IVs) and quantifies the strength of associations between them. We also should recognize that no statistical model comes without any assumptions (they sometimes get violated). No analysis is bias-free and these assumptions can introduce bias into the equation no matter how much we try to avoid it. It important to also consider the importance of knowing your data thoroughly before considering variables or selecting a model. For life sciences, it requires an intensive interplay between the PI of the research project (usually a nonstatistician) and the statistician in charge of designing and performing statistical analysis.

In ST518, I remember that depending on the method we chose, it came with a set of assumptions that we have to follow -- usually, assuming independence between observations and the observations following a certain distribution (normal, t, F, chi-square).

Example:  

Assumptions of the model:  
epsilon_i ~ iid (0, sigma^2)  
-	Normally distributed  
-	Centered at zero: E(epsilon) = 0  
-	Constant variance: Var(epsilon) = sigma^2  
-	Independent    

Routine work for a practicing statistician includes the development, estimation, and interpretation of statistical models for observational data geared towards answering research questions in life sciences -- this is most applicable to me as I work in drug development. 

Models mentioned in this field are as follows:  
- Predictive (or prognostic) models -- the aim to accurately predict an outcome value from a set of predictors  
- Explanatory models -- used in etiological research and should explain differences in outcome values by differences in explanatory variables  
- Descriptive models -- capture the association between dependent and independent variables

In the life sciences, models of all three types are needed. Still, they differ in the way they are used and interpreted.

.: How you would plan to determine variables to use in a regression model. :.

Variable selection is intended to select the best subset of predictors.

In a more general sense, we would consider what kind of data we are dealing with. I don't think that we can ever really escape Exploratory Data Analysis (EDA/EDA2) -- like the importance of using background knowledge to guide variable selection, seeing if there is missingness, outliers, influential points, patterns between vars, etc. Also, figuring out what to do with these findings. It is also mentioned that keeping it simple is the best way to see what to include. I would start here. Once we have a better understanding of our data I would consider either -- forward selection (FS), backward elimination (BE), Stepwise Selection, Tukey's Method, AIC, and BIC -- just out of familiarity. But, as mentioned previously, there are pitfalls to the choices that I make as a statistician without much experience. 

Our goal is to explain the data in the simplest way and removing redundant predictors. It really is a balance to consider - the smallest model that has the most significant variables is the best model. This also saves on time and money by not measuring redundant predictors!

.: What variable selection techniques do you prefer and why? :.  

The variable selection technique that I would prefer is probably one that was more familiar to me -- stepwise (combo of forward and backward selection), but I know that this has pitfalls/might not be my best option and I need to keep in mind. This seems most intuitive  to me because either we start with a model where we add one variable at a time, start with a full model and remove what we deem is insignificant after each run, or a combo of the two, respectively. Repeat this until all insignificant variables are removed or significant variables are added after each re-estimation. 
 
Also, just based of things I have heard over the years, Tukey's is something that I will / should use a lot in my course work / career.
 
After reading these articles it seems like the best option would be to use a method that is criterion-based because it typically involves a wider search and compares models in a preferable manner. For this reason, it is most recommended that we use a criterion-based method -- AIC or BIC.
 
- The Akaike information criterion (AIC)  
- The Bayesian information criterion (BIC) -- developed for situations where one assumes existence of a true model that is in the scope of all models that are considered in model selection.  

Things to Keep in Mind:
- Hypothesis tests are the most popular criteria used for selecting variables in practical modeling problems   
- Hierarchy of Terms -- keep the lower order terms associated with the higher order terms / interactions... (e.g. if x^2, keep x)
- Consider things that are too highly correlated and remove those  
- Programs can help with the computation - I'm more familiar with SAS Procedures -- Modeling techniques: PROC GLM, PROC REG, PROC LOGISTIC -- R and SPSS also available (need to be careful of the software capabilities)   
- Do not perform variable selection on IVs with known strong effects
- Keep in mind confounding factors	

Finding the best possible subset of variables to put in a model has been frustrating as many variable selection methods exist. I was not aware of all the pitfalls of my model selection methods. In the end, it looks like we just have to do our best to pick the best model out there for out specific data or else the conclusions might now be as telling.

Lastly, from article list below, I fall here --> 5, 7, 8, 9 (I'm sure all of them in one way or another)

Weaknesses/Downfalls of Modeling Techniques:

1. For All-subset selection with more than 40 variables:     
	(a) The number of possible subsets can be huge.    
	(b) Often, there are several good models, although some are unstable.    
	(c) The best X variables may be no better than random variables, if the size sample is relatively smaller than the total number of variables.    
	(d) The regression statistics and regression coefficients are biased.   
2. All-subset selection regression can yield models that are too small.   
3. The rationale for the number of candidate variables, and not the number in the final model, is the number of degrees of freedom to consider.   
4. The data analyst knows more than the computer and failure to use that knowledge produces inadequate data analysis.    
5. Stepwise selection yields confidence limits that are far too narrow.   
6. Regarding the frequency of obtaining authentic predictor and noise variables, the degree of correlation among the predictor variables affects the frequency with which authentic predictor variables can find their way into the final model. The number of candidate predictor variables can also affect the number of noise variables that gain entry to the model.    
7. Stepwise selection will not necessarily produce the best model if there are redundant predictors (a common problem).     
8. There are two distinct questions here: (a) When is Stepwise selection appropriate? and (b) Why is it so popular?   
9. As to question (b) above, there are two groups that are inclined to favor its usage. One consists of individuals, with little formal training in data analysis, who confuse knowledge of data analysis with knowledge of the syntax of SAS, SPSS and so on. They seem to feel that "if it's there in a program, it's gotta be good – and better than actually thinking about what my data might look like". They are fairly easy to spot and condemn in a group of well-trained data analysts. However, there is also a second group that is often well trained. Its members believe in statistics, but believe that given any properly obtained database, a suitable computer program can objectively make substantive inferences without active consideration of the underlying hypotheses. Stepwise selection is the parent of this blind data analysis

Other Useful Information from the Articles:

EDA includes the following characteristics:   
1. Flexibility – techniques with greater flexibility to delve into the data;   
2. Practicality – advice on procedures to analyze data;  
3. Innovation – techniques for interpreting results;   
4. Universality – use all of statistics that apply to analyzing data; and  
5. Simplicity – above all, the belief that simplicity is the golden rule.  

The Natural Seven-step Cycle of Statistical Modeling and Analysis  
1. Definition of the problem. Determining the best way to tackle the problem is not always obvious. Management objectives are often expressed qualitatively, in which case the selection of the outcome or target (dependent) variable is subjectively biased. When the objectives are clearly stated, the appropriate dependent variable is often unavailable, in which case a surrogate must be used.   
2. Determining technique. The technique first selected is often that with which the data analyst is most comfortable, and not necessarily the best technique for solving the problem.   
3. Use of competing techniques. Applying alternative techniques increases the odds that a thorough analysis is conducted.   
4. Rough comparisons of efficacy. Comparing the variability of results across techniques can suggest additional techniques or the deletion of alternative techniques.
5. Comparison in terms of a precise (and thereby inadequate) criterion. An explicit criterion is difficult to define;  therefore, precise surrogates are often used.
6. Optimization in terms of a precise and similarly inadequate criterion. An explicit criterion is difficult to define; therefore, precise surrogates are often used.
7. Comparison in terms of several optimization criteria. This constitutes the final step in determining the best solution.  

<!--
Your blog post can be written in a conversational tone or more formally (however you want to represent yourself).  There is no word count or anything like that, just make sure you answer the prompts above to receive full credit.

Submit the URL for your (rendered) github blog in the text box. 
-->
