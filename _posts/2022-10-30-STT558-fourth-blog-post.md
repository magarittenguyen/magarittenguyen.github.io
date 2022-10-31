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
Exploratory Data Analysis (EDA) can be a very large area of focus. When handed a dataset and then being asked to describe it, EDA is an critical tool/approach/philosophy, used by data scientists, for data analysis and is primarily used to investigates data sets by using many different techniques (usually via statistical graphics and other data visualization methods) to maximize insight on / see what can be revealed about a given data set beyond the formal modeling and therefore differs in comparision to traditional hypothesis testing.

EDA was promoted by American mathematician John Tukey since 1970 and is essential because it encourages statisticians to explore the data. This can be done with or without a formal statistical model and is meant to summarize the main characteristics of the given data set by providing a better understanding of the missingness behind the data, the variables and the relationships/patterns/correlation between/within them before making any assumptions, and detect outliers in the data set. This helps to determine how best to manipulate data sources to get invaluable answers you need to some of those crucial business questions, which makes it easier for data scientists to discover, again, significant patterns and outliers -- leading data scientists to possibly formulate hypotheses for why these patterns occur or assess their assumptions (helps determine if the statistical techniques you are considering for data analysis are appropriate), which could lead to further/new data collection and experiments -- enabling unexpeted discoveries. EDA can also help identify obvious errors in your approach (appropriate statistical tools and techniques) and it is made clear that taking notes thorughout this entire process is very important. This helps data scientists to hpothesize about the causes of observed phenomena as they perform the EDA and this technique continues to be a widely used method in the data discovery process today.

Before you start exploring the data, its important to know what the intended outcome of your EDA will be and to gain as much context as possible in order to have a high level understanding of your data (e.g. What kind of data is this? What is it about?), which will help focus your efforts. Sometimes this could lead to subsampling your dataset in the case tha it is too big to avoid compulational bottlenecking that may occur later on. You can do this by observing the first couple of rows of the data and trying to identify what makes each row (samples) unique. 

When looking at the data itself you want to:

I. Check For Missing Data 

A great place to start looking at your data is to look at the missing data and trying to understand/hypothesize the underlying reason behind its missingness and have a plan on how to deal with them. For example, we can't just get rid of these observations because it will introduce bias into your dataest. One technique is to rank the columns by least missing to most missing and looking into the columns one by one. Missing data is also a feature and should be looked at too.

II. Provide Basic Descriptions of Your Sample and Features 

Providing a basic description of your features and categorizing them helps with this step. This will drastically change the visualizations you use and the statistical methods you apply. For instnace, we want to see how many rows (samples) and columns (features) are in the dataset. Also, we want to ask ourselves -- is it a reasonable sized data to work with? If not, how can we subsample as mentioned above. Ask questions like -- What is a unique identifier? How are the rows unique? What are their ranges? We can also look at each column, one at a time, to plan for future analaysis. Depending on the type of data, we can create different graphs to look at the data -- continuous, discrete, categorical. This dictates how we move forawrd because diffrent data requires differnt techniques/statitical method and viusliation (its not one size fits all)).

III. Identify The Shape of Your Data 

Understand your data by visualizing its distribution/shape. Get comfortable with how your data changes across samples and over time. Some ways ot do this are with via PMF or PDF. Look at mean and variance of each featurr, look into the reasons behind any drastic changes, patterns, low/high values and hypothesize the reason behind this behavior. 

Here a few things that PMFs and PDFs can tell you about your data: 
 
- Skewness
- Is the feature heterogeneous (multimodal)?
- If the PDF has a gap in it, the feature may be disconnected.
- Is it bounded?
        
Other common types of multivariate graphics include:

- Scatter plot, which is used to plot data points on a horizontal and a vertical axis to show how much one variable is affected by another.
- Multivariate chart, which is a graphical representation of the relationships between factors and a response.
- Run chart, which is a line graph of data plotted over time.
- Bubble chart, which is a data visualization that displays multiple circles (bubbles) in a two-dimensional plot.
- Heat map, which is a graphical representation of data where values are depicted by color.

IV. Identify Significant Correlations 

Make note of the reationships you see between your features. Meaning can be drawn from this down the raod. For example, the easiest way to visualize correlation is with a scatter plot or if high number of features to save time create a Pearson correlation matrix for your dataset.  

V. Spot Outliers in the Dataset 

A crucial step in EDA. Outliers can influence your findings if you don’t know about them or how to deal with them, so make sure you can identify them and have a plan to deal with them.

Tools that can help this process are programming languages such as R and Python.

I think that the overall goal when doing an EDA is:

> - to maximize insight into a data set
> - uncover underlying structure of the data / summarise their main characteristics
> - extract important variables (features/factors)
> - detect outliers and anomalies
> - test underlying assumptions
> - develop a cost effective models
> - determine optimal factor settings

Other Information that can be helpful:

There are four primary types of EDA:

- Univariate non-graphical. This is simplest form of data analysis, where the data being analyzed consists of just one variable. Since it’s a single variable, it doesn’t deal with causes or relationships. The main purpose of univariate analysis is to describe the data and find patterns that exist within it.

- Univariate graphical. Non-graphical methods don’t provide a full picture of the data. Graphical methods are therefore required. Common types of univariate graphics include:

> - Stem-and-leaf plots, which show all data values and the shape of the distribution.
> - Histograms, a bar plot in which each bar represents the frequency (count) or proportion (count/total count) of cases for a range of values.
> - Box plots, which graphically depict the five-number summary of minimum, first quartile, median, third quartile, and maximum.
        
- Multivariate nongraphical: Multivariate data arises from more than one variable. Multivariate non-graphical EDA techniques generally show the relationship between two or more variables of the data through cross-tabulation or statistics.

- Multivariate graphical: Multivariate data uses graphics to display relationships between two or more sets of data. The most used graphic is a grouped bar plot or bar chart with each group representing one level of one of the variables and each bar within a group representing the levels of the other variable.

Specific statistical functions and techniques you can perform with EDA tools include:

- Clustering and dimension reduction techniques, which help create graphical displays of high-dimensional data containing many variables.

- Univariate visualization of each field in the raw dataset, with summary statistics.

- Bivariate visualizations and summary statistics that allow you to assess the relationship between each variable in the dataset and the target variable you’re looking at.

- Multivariate visualizations, for mapping and understanding interactions between different fields in the data.

- K-means Clustering is a clustering method in unsupervised learning where data points are assigned into K groups, i.e. the number of clusters, based on the distance from each group’s centroid. The data points closest to a particular centroid will be clustered under the same category. K-means Clustering is commonly used in market segmentation, pattern recognition, and image compression.

- Predictive models, such as linear regression, use statistics and data to predict outcomes.
-->

<!--
Your blog post can be written in a conversational tone or more formally (however you want to represent yourself).  There is no word count or anything like that, just make sure you answer the prompts above to receive full credit.

Submit the URL for your (rendered) github blog in the text box. 
-->
