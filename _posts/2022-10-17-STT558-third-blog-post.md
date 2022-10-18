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



Exploratory Data Analysis (EDA) was promoted by American mathematician John Tukey since 1970. It is an approach/philosophy, used by data scientists, for data analysis and is primarily used to investigates data sets by using many differnt techniques (usually via statistical graphics and other data visualization methods) to maximize insight on / see what can be revealed about a given data set with or without a formal statistical model by summarizing the main characteristics of the given data set and providing a better understanding of data set variables and the relationships between them before making any assumptions. It helps determine how best to manipulate data sources to get the answers you need, making it easier for data scientists to discover patterns, spot anomalies, test a hypothesis, or check assumptions.

EDA is primarily for seeing what the data can tell us beyond the formal modeling and thereby contrasts traditional hypothesis testing. adn this technique continues to be a widely used method in the data discovery process today.




EDA can be a very large area of focus

It can also help determine if the statistical techniques you are considering for data analysis are appropriate.

 It can help identify obvious errors, as well as better understand patterns within the data, detect outliers or anomalous events, find interesting relations among the variables.




A strategy I would use for EDA after reading the selected artilces provided is as follows:

.: *What is your overall goal when doing an EDA?* :.

I think that the over all goal when doing an EDA is:
    uncover underlying structure / summarise their main characteristics;
    extract important variables;
    detect outliers and anomalies;
    test underlying assumptions;
    develop parsimonious models; and
    determine optimal factor settings.


By encouraging statisticians to explore the data, they can possibly formulate hypotheses, which could lead to further/new data collection and experiments.  



   








 






> 
> 
> tools R and Python... 

The objectives of EDA are to:

    Enable unexpected discoveries in the data
    Suggest hypotheses about the causes of observed phenomena
    Assess assumptions on which statistical inference will be based
    Support the selection of appropriate statistical tools and techniques
    Provide a basis for further data collection through surveys or experiments[7]

 






By performing an EDA, you might answer some of those crucial business questions we alluded to earlier.
The reality is that exploratory data analysis (EDA) is a critical tool in every data scientist’s kit, and the results are invaluable for answering important business questions
 been handed a dataset and then been asked to describe it
 Simply put, an EDA refers to performing visualizations and identifying significant patterns, such as correlated features, missing data, and outliers. EDA’s are also essential for providing hypotheses for why these patterns occur. It most likely won’t appear in your data product, data highlight, or dashboard, but it will help to inform all of these things.

.: *What methods do you think are important?* :.

Some methods that I think are important when carrying out an EDA are:


> Before you start exploring the data, you should try to understand the data at a high level.  Speak to leadership and product to try to gain as much context as possible to help inform where to focus your efforts. Are you interested in performing a prediction task? Is the task purely for exploratory purposes? Depending on the intended outcome, you might point out very different things in your EDA.
> noce you inderstand that , time to look at your dataset how many samples (rows) and how many features (columns) are in your dataset, keep in mind subsampling your dataset it too big to avoid computationa bottlenecking that may occur down the road; observe first couple of rows to see the type of data you are workign with
> question to address,... What is the unique identifier of each row in the data?

- what kind of data, what is it about
- how many rows and cols sample features
- reasonable size to work wiht?
- -what is a unique idnitier ? one obs of data per row
- how may unique tings
- what re their ranges

start: looking at data itself
- check for missing data good plce to start
- look at features one at a time (cols) for analysis and future ananysis
- rank cols / features by how much missing they have large to smal l (some say remove - dont!) but understand why missing ansd see behavior
- could be a reson why feature left balnk
- hyphtesize why
- if we remove wihtout thinking about it we intorduce bias into out data...
- Therefore, this missing data is a feature in its own right and should be treated as such.
- - what does missingness mean?
- no simple answer
- imputation () linear interpolatoin () -- approach depends on data type

2. categorize your features 
 continuous, discrete, categorical -dictates how we move forwardbecuase diff data requires diff techinqes/statitical method and viusliation (its not one size fits all )

3. look at th shape (pmf pdf) of your feature, mean , variance after for each feature
 any chages? patters? hypothesize behavior
 low high vaiance? - addtional invetigation
Here a few things that PMFs and PDFs can tell you about your data: 
 
    Skewness
    Is the feature heterogeneous (multimodal)?
    If the PDF has a gap in it, the feature may be disconnected.
    Is it bounded?

 
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


important to take notes thorughout this process.

Before You Start
1. Check For Missing Data
2. Provide Basic Descriptions of Your Sample and Features
3. Identify The Shape of Your Data
4. Identify Significant Correlations
5. Spot Outliers in the Dataset
What’s Next?

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
