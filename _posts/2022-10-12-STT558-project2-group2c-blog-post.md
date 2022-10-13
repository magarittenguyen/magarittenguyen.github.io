## ST558 - Project 2  
### Group 2C

<!--
Overview

This project is to create a vignette for reading in data from an API.  Assesses many LOs (emphasis on 2.3, 2.4, 3.2, 3.4, 4.2, 4.5, 5.4, 6.1, 6.5, and 6.6)
Completion time

The estimated time to complete this assignment is 12-20 hours.
Instructions

   - The instructions can be found in the attached PDF document.
   - You must keep your github repo private until the due date.
   - Submit the URL for the rendered blog post you make.

Groups
Group memberships. If you need this to be more accessible, let me know!
Suyog & Magaritte
-->

<!--
Submission
Once your group has completed their vignette, each group member should write a brief blog post on their
own github.io blog site. The blog post should:
• explain what you did in the project and any interesting findings
• reflect on the process you went through for this project. Discuss things like:
– what was the most difficult part of the logic and programming for you?
– what would you do differently in approaching a similar project in the future?
• provide a link to the rendered github pages repo and the regular repo (non-github pages
site) as well!
The URL to this (rendered) blog post is what each individual will submit at the project assignment link.
-->

### Instructions  
#### Once your group has completed their vignette, each group member should write a brief blog post on their own github.io blog site.

The blog post should:   

• explain what you did in the project and any interesting findings   
• reflect on the process you went through for this project. Discuss things like:    

  > – what was the most difficult part of the logic and programming for you?  
   
  > – what would you do differently in approaching a similar project in the future?  
      
________________________________________________________________________________________
________________________________________________________________________________________
   
.: *Project Purpose, Tasks, and Interesting Findings* :.

Hooray! Another Project in the books and I still didn't die too bad. This is probably because I had someone to share the burden of dying with. Woo.

For our second project in ST558 - Data Science for Statisticians, we are asked to work through the Project 2 instructions provided and create a vingette that explains how to contact an API, from a selection, using functions that we have created to query, parse, and return well-structured data. We then use our functions to obtain data from a particular API (Spoonacular Food and Recipe API) in order to do some exploratory data analysis. 

Our report is written up in an `R Markdown` file that is linked with the `GitHub` repositiry, that will render a `github_document`. We also had to write a narrative in order to show that we fully understood each step carried out and assess many Learning Objectives from Topic 1 and Topic 2.

This project was done in pairs and my partner was Suyog Shekhar Dharmadhikari. We had to collaborate via a `Github` repository. For this project I think that both Suyog and I did a good job collaborating, deligating, and making time to work through challenges. We made sure to reach out early on and kept in touch as we worked on the respective parts of the project. We reached out to each other before Fall break via e-mail to initiate a conversation and schedule times to meet just to make a first pass at the project and go over the directions. We then set up calls and video chats periodically to deligate and create a game plan. We texted often. Since he is more familiar with GitHub as a Masters Computer Science student, he set up the repo, walked me through what he had done, and help me link `GitHub` and `RStudio` - reinforcing what we have seen in lecture.

While he was away for fall break, I was able to set up create the render file and get started on the `YAML` header and code chunks for the project. I started by creating a `API key` for the `Spoonacular` API and looking at all the different types of queries we could have in our function. I worked on the function `my_Spoonacular_API` and got it to a point where I would explain to Suyog what I had done and let him include modifications, like more parameters (`diet`, `minProtein` and `maxProtein`), to it. I also made sure that there was a return message if a user were to define a `cuisinetxt` type that was not listed in the `Spoonacular` API that prompted them what types of things they could enter. 

Once we had our first function running, I called it twice and saved the results to an object. While testing I noticed that for the keyword `ingredient`="fruit", the most recpies returned was for the "American" cuisine. So, I decided to use this for my exploratory data analysis (EDA). I forgot to mention that our function also has an option to append nutrient info to it. But, to access more nutrient info, I had to index a list of list in a couple more levels. 

I created a new object called `nutrients` that looked at `calories`, `carbs`, `protein`, and `fat`. I go on to append a five number summary of protien (g) content in the recipes to the `nutrient` object. I also add on a variable for the total price of the recipe in USD (`totalprice`) and a variable for grams of protein per serving of food in a recipe (`protein_per_serving`).

With this data I created contingency tables. One, looking at the association of `vegan` and `vegetarian` recipes, one looking at sources where the recipes came from and how healthy they were, and lastly sources of where the recipes came from and weather or not they wre expensive -- expensive meaning that the price was higher than the 75% percentile of the data. I also create a couple of boxplots, scatter plots, and had a regression line overlaying a scatter plot.

Every time we met, we would explain to each other what the other person had done and continue to deligate tasks. One way we got through not having to reconcile program merge diffrences too much was to comminucate when we were going to pull, commit, and push. Suyog had a sub repo branch he was working on and would monitor the main repo for my commits and deal with the merging conflicts as they came in. He would show me his process here and there. We did this often in small sections, so I thought that this was very helpful. 

We spent time apart and together writing our narrative and then proof reading it for a couple hours on the day it was due. We also tried to draw conclusions the best we could from our EDA.

I think we made a good team. we tried to meet before HW6 was due, the exam, and over fall break. We were good at reaching out and starting a conversation. 


In summary, the process of our project is as follows:  

> - Set up `GitHub` Repo  
> - Give access to second member   
> - Set up and sync to `RStudio` in compauter to `GitHub` Repo  
> - Create `README.md` file for rendering  
> - Know that the `RMarkdown` page and the render file are seperate files  
> - Call an API, we chose the Spoonacular Food and Recipe API  
> - Figuring out how to aceess and parse the data -- HW4 (API) and HW5 (plotting) were useful  
> - Once we could get it to work for one scenario, we created a function  
> - Built functions to interact with some of the Spoonacular Food and Recipe API endpoints like `ComplexSearch` and `findByNutrients`  
> - Retrieved some of the data based on different user modifications  
> - Called function for atleast two situations - 6 endpoints - we chose (cuisine type, recipe ingredient, number of observations that could be returned (max 100), appending on nutrient info, diet type, min protein, max protien)  
> - Once we ran 2 senarios we started to do EDA  
> - Contingency tables (remeber no meaning is intended beacuse... we didnt know what we were searching for, but we're just kind of "farting around in the dark...")  
> - Added few new variables from ones we had  
> - Added summary stats like a five number summary on protein content (g) ...  
> - Plotting: bar charts/graphs, histogram, boxplot, scatterplot overlay, own scatter plot, scatter plot with regression over lay (mostly looking at protein content in vegan and vegatarian food)  
> - During this entire process we had to communicate and pull, commit, and push as necessary


Some interesting findings for our specific vingette examples:  

> - Some vegetarian recipes are vegan as well  
> - Most of the unhealthy food recipes are from the *Foodista* source  
> - Recipes suggested by *Foodista* has the maximum number of expensive recipes, but also suggests maximum number of inexpensive recipes  
> - `Cinnamon French Toast Sticks` has a higher protein content than a non vegetarian meals like the `Turkey Burgers with Slaw`, even though it is a vegetarian recipe. This is surprising, but also makes sense due to the high protein content in eggs.  
> - It can be seen that the number of "American" cuisine recipes are much higher in comparison to "Chinese" and "Latin American" cuisines for our vignette for the recipes containing "fruit".  
> - The protein content in non vegetarian meals in generally much greater than the protein content in vegetarian meals - as expected  
> - When broken down by serving, the protein content in vegetarian meals (for some) have a higher protein content then the non vegetarian meals  
> - There is no real pattern to be observed between carbohydrates and protein  
> - The regression line basically has no change in protein (g) at any amount of carbohydrates, confirming our plot that is only a scattet plot between protein and carbohydrates  
 

.: *Project Process: Difficulties in Logic & Programming, Future Approach On Similar Project* :.

Some things that I found difficult were:

> - Remebering that I needed to apply and get a key in order to access the API (getting a key)
> - How to enter the keywords into my function, so that the url would recognize what we wanted, (I had to look at the documentation and there was a lot of trial and error here)
> - Trying to grab / index things that I wanted (dealing with lists of lists of lists to get to a data frame for example)
> - I ran into an issue with words that were seperated by a space for my cusine (e.g. Latin America) and retuning 0 results for recipies, but that was not true
> - I thought it was clever to add my note that said text needed to be entered that matched the possible list of cuisines, but had a hard time with that as well
> - Tried entering more than one cuisine, but had no luck -- Suyog did it, but it is a seperate function (wondering how I could have added it to my function, maybe with more time)


Some things that I would do differently:

> - Try to start earlier, it was over fall break and some plans that had been made, made it difficult to meet up and work together
> - Most of the work was meeting, delegating, and working on our own - not sharing screens as much, like we took sections, it wasnt like we worked on all the sections together by sharing screens/ logic (at first). But, we did walk each other through what we did the next day and expalined our logic. Not sure which approach is best... (ended up working together a lot more towards the end) 
> - I wasnt sure how to set up the repo stuff but my partner has more experisnce using is because hes going for a master in computer scinece and was well versed. That was great to have someone with experince with this. My only exposure has been in this class... 
> - Spend more time on my typography choices(?) again. 
> - Tried to write the narrative and edit my comments as I was completing the project because going back over it would have just been proof reading and checking spacing once 
> - I always feel like I should start sooner rather than later, even though I did start pretty early on this project. (I always wish I have more time, but I think we did a good job with the time we had.)

Is it bad that I still feel the same as for the last project?

________________________________________________________________________________________
________________________________________________________________________________________

.: *Links:* :.

[Main Page of Blog Posts Link](https://magarittenguyen.github.io/)
 
[Project 2 Blog Post Link](https://magarittenguyen.github.io/2022/10/12/STT558-project2-group2c-blog-post.html)

[Vingette Link](https://pages.github.ncsu.edu/sdharma2/ST558_Project_2_C/)

[Project 2 GitHub Repo Link](https://github.ncsu.edu/sdharma2/ST558_Project_2_C)

[HTML Link of Vignette](https://magarittenguyen.github.io/README.html)


Thank you!
