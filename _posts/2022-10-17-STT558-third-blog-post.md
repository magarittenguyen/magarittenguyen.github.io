## ST558 - My Third Blog Post  

<!--
Overview

This assignment is to create a blog post using your github blog.  See below for the blog post prompt. Assesses LO 1.3 and others.
Completion time

The estimated time to complete this assignment is 20-40 minutes.
Instructions
-->

### Instructions  
#### Write a blog post to respond to the prompt below:

#### Exploratory Data Analysis (EDA) is often the first step of dealing with data.  However, EDA is somewhat of an art and something that you get better at with experience.  Often people new to EDA don't know what they should be looking for!  Read through these articles (and others if you'd like to find your own):  

> https://shopify.engineering/conducting-exploratory-data-analysis  
> https://www.ibm.com/cloud/learn/exploratory-data-analysis  
> https://en.wikipedia.org/wiki/Exploratory_data_analysis  
> https://www.itl.nist.gov/div898/handbook/eda/section1/eda11.htm  

For your blog post, write up the strategy you use for EDA. What is your overall goal when doing an EDA? What methods do you think are important? What things do you try to look for? 

.: *What is your overall goal when doing an EDA?* :.

Exploratory Data Analysis (EDA) can be a very large area of focus. When handed a dataset and then being asked to describe it, EDA is an critical tool/approach/philosophy, used by data scientists, for data analysis and is primarily used to investigates data sets by using many differnt techniques (usually via statistical graphics and other data visualization methods) to maximize insight on / see what can be revealed about a given data set beyond the formal modeling and therefore differs in comparision to traditional hypothesis testing.

EDA was promoted by American mathematician John Tukey since 1970 and is essential because by encouraging statisticians to explore the data. This can be done with or without a formal statistical model and is meant to summarize the main characteristics of the given data set by providing a better understanding of the missingness behind the data, the variables and the relationships/patterns/correlation between/within them before making any assumptions, and detect outliers in the data set. This helps to determine how best to manipulate data sources to get invaluable answers you need to some of those crucial business questions, which makes it easier for data scientists to discover, again, significant patterns and outliers -- leading data scientists to possibly formulate hypotheses for why these patterns occur or check thier assumptions (helps determine if the statistical techniques you are considering for data analysis are appropriate), which could lead to further/new data collection and experiments. EDA can also help identify obvious errors in your approach and it is made clear that taking notes thorughout this entire process is very important.

Tools that can help this process are programming languages such as R and Python.

I think that the overall goal when doing an EDA is:

> - to maximize insight into a data set
> - uncover underlying structure of the data / summarise their main characteristics
> - extract important variables (features/factors)
> - detect outliers and anomalies
> - test underlying assumptions
> - develop a cost effective models
> - determine optimal factor settings





> enable unexpected discoveries in the data (done)
> suggest hypotheses about the causes of observed phenomena (might answer some of those crucial business questions // the results are invaluable for answering important business questions)
> assess assumptions on which statistical inference will be based
> support the selection of appropriate statistical tools and techniques
> provide a basis for further data collection through surveys or experiments
    



This technique continues to be a widely used method in the data discovery process today.







.: *What methods do you think are important?* :.

Some methods that I think are important when carrying out an EDA are:



Before you start exploring the data, its important to know what the intended outcome of your EDA will be and to gain as much context as possible in order to have a high level understanding of your data (e.g. What kind of data is this? What is it about?), which will help focus your efforts. Sometimes this could lead to subsampling your dataset in the case tha it is too big to avoid compulational bottlebecking that may occur later on. You can do this by observing the first couple of rows of the data and trying to identify what makes each row (samples) unique. 

When looking at the data itself you want to:

1. Check For Missing Data (Great place to start. Underlying reason behind missingness - why and see behavior, hypothesize why; can't just get rid of these observations because it will introduce bias into your dataest. Rank the columns by least missing to most missing. Missing data is also a feature and should be looked at too.)

2. Provide Basic Descriptions of Your Sample and Features (How many rows (samples) and columns (features)? Is it a reasonable sized data to work with? What is a unique identifier? How are the rows unique? What are their ranges? Look at each column at a time to plan for future analaysis. Depending on the type of data, we can create different graphs to look at the data -- continuous, discrete, categorical. this dictates how we move forawrd because diffrent data requires differnt techniques/statitical method and viusliation (its not one size fits all))

3. Identify The Shape of Your Data (via pmf, pdf, -- look at mean, variance of each feature. Look into reasons behind any drastic changes, patterns, low/high values for e.g. variance of each feature. hypothesize this behavior. )

Here a few things that PMFs and PDFs can tell you about your data: 
 
    - Skewness
    - Is the feature heterogeneous (multimodal)?
    - If the PDF has a gap in it, the feature may be disconnected.
    - Is it bounded?

4. Identify Significant Correlations

5. Spot Outliers in the Dataset


What’s Next?


 
 4. Correlation measures the relationship between two variable quantities. The easiest way to visualize correlation is by plotting a scatter plot 
 If you have a high number of features in your dataset, then you can’t create this plot for all of them—it takes too long. So, I recommend computing the Pearson correlation matrix for your dataset. 
 assigns a value between -1 and 1 to each feature pair.
 A positive value indicates a positive relationship and a negative value indicates a negative relationship.
 
5. Last, but certainly not least, spotting outliers in your dataset is a crucial step in EDA. 



    1 Missing values can plague your data. Make sure to understand why they are there and how you plan to deal with them.
   2  Provide a basic description of your features and categorize them. This will drastically change the visualizations you use and the statistical methods you apply.
    3 Understand your data by visualizing its distribution. You never know what you will find! Get comfortable with how your data changes across samples and over time.
    4 Your features have relationships! Make note of them. These relationships can come in handy down the road.
    5 Outliers can dampen your fun only if you don’t know about them. Make known the unknowns!




.: *What things do you try to look for?* :.

Some things that I would try to look for while carrying out an EDA are:
> 

There are four primary types of EDA:

    Univariate non-graphical. This is simplest form of data analysis, where the data being analyzed consists of just one variable. Since it’s a single variable, it doesn’t deal with causes or relationships. The main purpose of univariate analysis is to describe the data and find patterns that exist within it.
    Univariate graphical. Non-graphical methods don’t provide a full picture of the data. Graphical methods are therefore required. Common types of univariate graphics include:
        Stem-and-leaf plots, which show all data values and the shape of the distribution.
        Histograms, a bar plot in which each bar represents the frequency (count) or proportion (count/total count) of cases for a range of values.
        Box plots, which graphically depict the five-number summary of minimum, first quartile, median, third quartile, and maximum.
    Multivariate nongraphical: Multivariate data arises from more than one variable. Multivariate non-graphical EDA techniques generally show the relationship between two or more variables of the data through cross-tabulation or statistics.
    Multivariate graphical: Multivariate data uses graphics to display relationships between two or more sets of data. The most used graphic is a grouped bar plot or bar chart with each group representing one level of one of the variables and each bar within a group representing the levels of the other variable.

Other common types of multivariate graphics include:

    Scatter plot, which is used to plot data points on a horizontal and a vertical axis to show how much one variable is affected by another.
    Multivariate chart, which is a graphical representation of the relationships between factors and a response.
    Run chart, which is a line graph of data plotted over time.
    Bubble chart, which is a data visualization that displays multiple circles (bubbles) in a two-dimensional plot.
    Heat map, which is a graphical representation of data where values are depicted by color.


Specific statistical functions and techniques you can perform with EDA tools include:

    Clustering and dimension reduction techniques, which help create graphical displays of high-dimensional data containing many variables.
    Univariate visualization of each field in the raw dataset, with summary statistics.
    Bivariate visualizations and summary statistics that allow you to assess the relationship between each variable in the dataset and the target variable you’re looking at.
    Multivariate visualizations, for mapping and understanding interactions between different fields in the data.
    K-means Clustering is a clustering method in unsupervised learning where data points are assigned into K groups, i.e. the number of clusters, based on the distance from each group’s centroid. The data points closest to a particular centroid will be clustered under the same category. K-means Clustering is commonly used in market segmentation, pattern recognition, and image compression.
    Predictive models, such as linear regression, use statistics and data to predict outcomes.






<!--
Your blog post can be written in a conversational tone or more formally (however you want to represent yourself).  There is no word count or anything like that, just make sure you answer the prompts above to receive full credit.

Submit the URL for your (rendered) github blog in the text box. 
-->
