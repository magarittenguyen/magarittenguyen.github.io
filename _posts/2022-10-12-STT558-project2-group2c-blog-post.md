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
      
   
.: *Project Purpose, Tasks, and Interesting Findings* :.

Hooray! Another Project in the books and I still didn't die too bad. This is probably because I had someone to share the burden of dying with. Woo.

For our second project in ST558 - Data Science for Statisticians, we are asked to work through the Project 2 instructions provided and create a vingette that explains how to contact an API, from a selection, using functions that we have created to query, parse, and return well-structured data. We then use our functions to obtain data from a particular API (Spoonacular Food and Recipe API) in order to do some exploratory data analysis. 

Our report is written up in an R Markdown file that is linked with the GitHub repositiry, that will render a GitHub Document. We also had to write a narrative in order to show that we fully understood each step carried out and assess many Learning Objectives from Topic 1 and Topic 2 that we have learned.

This project was done in pairs and my partner was Suyog Shekhar Dharmadhikari. We had to collaborate via a Github repository. For this project I think that both Suyog and I did a good job collaborating, deligating, and making time to work through challenges. We made sure to reach out early on and kept in touch as we worked on our respective parts of the project. We reached out to each other befire Fall break via e-mail to initiate a conversation and schedule times to meet just to make a fisrt pass at the project. We then set up calls and video chats periodically to deligate and create a game plan. We texted often. Since he is more familiar with GitHub as a Masters Computer Science student, he set up the repo, walked me through what he had done, and help me link GitHub and RStudio - reinforcing what we have seen in lecture.

While we was away for fall break, I was able to set up create the render file and get started on the YAML header and code chunks for the project. I started by creating a API key for the Spoonacular API and looking at all the different types of queries we could have in our function. I worked on the function `my_Spoonacular_API` and got it to a point where I would explain to Suyog what I had done and let him include modifications, like more parameters (diet, min and max protein), to it. I also made sure that there was a return message if a user were to define a cuisine type that was not listed in the Spoonacular API that prompted them what types of things they could enter. 

Once we had our first function, I called it twice and saved the object. While testing I noticed that for the keyword "fruit", the most recpies returned was for the Aerican cuisine. So, I decided to use this for my exploratory data analysis (EDA). I forgot to mention that our function also has an option to append nutrient data to it. But, to access more nutrient info, I had to index a list of list in a couple more levels. 

I created a new object called nutrients that looked at calories, carbs, protein, and fat. I go on to append a five number summary of protien (g) content in the recipies to the nutrient object. I also add on a variable for the total price of the recipie in USD and a variable for grams of protein per serving of food in a recipe.

With this data I created contingency tables. One, looking at the association of vegan and vegetarian food, one lookng at sources where the recipies came from and how healthy they were, and lastly sources of where the recipies came from and weather or not they wre expensive -- expensive meaning that the price was higher than the 75% percentile of the data. I also create a couple of boxplots, scatter plots, and have a regression like overlaying a scatter plot.

We spent time apart and together writing our narrative and proof reading it for a couple hours. We also tried to draw conclusions the best we could from out EDA.

In summary, the process of our project is as follows:  

> - Set up GitHub Repo  
> - Give access to second member   
> - Set up and sync to RStudio in compauter to GitHub Repo  
> - Create README.md file for rendering  
> - Know that the RMarkdown page and the render file are seperate files  
> - Call an API, we chose the Spoonacular Food and Recipe API  
> - Figuering out how to aceess and parse the data -- HW4 (API) and HW5 (plotting) were useful  
> - Once we could get it to work for one scenario, we created a function  
> - Built functions to interact with some of the Spoonacular Food and Recipe API endpoints like ComplexSearch and findByNutrients  
> - Retrieved some of the data based on different user modifications  
> - Called function for atleast two situations - 6 endpoints - we chose (cuisine, recipe, ingredient, number of obs that could be returned (max 100), diet, min protein, max protien)  
> - Once we ran 2 senarios we started to do EDA  
> - Contingency tables (remeber no meaning is intended beacuse... we didnt know what we were searching for, but just kind of "farting around in the dark...")  
> - Added few new vars from ones we had  
> - Added summary stats like a five number summary on protein content (g) ...  
> - Plotting: bar, histogram, boxplot, scatterplot overlay, own scatter plot, scattter plot with regression over lay (mostly looking at protein content in vegan and vegatarian food)  
> - Some interesting findings, there are recipes that have higher protein content than even non vegetarian reipes... makes sense eggs high protein (especially egg whites)  


Some interesting findings for our specific vingette examples:  

> - Some vegetarian recipes are vegan as well  
> - Most of the unhealthy food recipes are from the *Foodista* source  
> - Recipes suggested by *Foodista* has the maximum number of expensive recipes, but also suggests maximum number of inexpensive recipes  
> - Cinnamon French Toast Sticks has a higher protein content than a non vegetarian meals like the Turkey Burgers with Slaw, even though it is a vegetarian recipe. This is surprising, but also makes sense due to the high protein content in eggs  
> - It can be seen that the number of American cuisine recipes are much higher in comparison to Chinese and Latin American cuisines for our vignette for the recipes containing fruit.  
> - The protein content in non vegetarian meals in generally much greater than the protein content in vegetarian meals as expected  
> - When broken down by serving, the protein content in vegetarian meals (for some) have a higher protein content then the non vegetarian meals  
> - There is no real pattern to be observed between carbohydrates and protein  
> - The regression line basically has no change in protein (g) at any amount of carbohydrates, confirming out plot that is only a scattet plot between protein and carbohydrates  
 

.: *Project Process: Difficulties in Logic & Programming, Future Approach On Similar Project* :.

Some things that I 

What I learned through this entire project is that programming is frustrating - especially if you're working on one screen. Being organized in you program is important to -- like keeping parethases in check, because it can get very confusing. I had to label my closing parenthases so that I wouldn't get lost. I copied all the directions over first and then commented as much as I could as I completed the project. This helped a lot because I didn't have to flip back and forth between applicaitons. I reinforced what functions go to which tidyverse toolkit/package because that was a bit confusing at first, but I think that comes with practice/exposue. I got to learn funcitons more carefully just by looking up how to use them and explaining with the narrative. I have some SAS knowledge, so it was interesting to see how certain things are programmed in R. I also didn't realize you could reference a variable in a dataset without merging/combining it first. It was the step where we had to pick the x amount of states from the manipulated dataset in order to pick those states in the orgional dataset and plot those observations. I also learned how to use nested ifelse() functions. That part was very tedious to me.

.: *what you would do differently, etc.* :.

Some things that I would do differntly is spend more time on my typography choices(?). I'm not sure I realy did those correctly, but I pretty much put the tick symbols around anything I thought was important coding wise. I also would have tried to write the narrative and edit my comments as I was completing the project because going back over it would have just been proof reading and checking spacing once - rather than having to go back many more times making sure I understood what I was doing again after the fact and losing my train of thought. Lastly, I always feel like I should start sooner rather than later, even though I did start pretty early on this project.





##########################################
##########################################
##########################################



  
  - reflect on the process you went through for this project. Discuss things like: (above)
  
    + what was the most difficult part of the logic and programming for you? 
    
> trying to access the api (getting a key)
> how to enter the keywords in so that the url will recognize what we want, had to look at the documentaiotn and there was a lot of trial and error
> also trying to grab / index thins that i wanted. 
> ran into an issue with words that were seperated by a space retuning 0
> thought it was clever to add my note that said text needed to be entered that matched the possible list of cuisines... 
> (tried entering more than one cuisine but ran out of time) partner did it but it is seperate, wondering if we should keep the function and name it somehting else or if it is redundant... 

    + what would you do differently in approaching a similar project in the future?  
    
> try to start earlier, it was over fall break and some plans that had been made it difficult to meet up and work together
> most of the work was meeting, delegating and working on our own, no sharing screens as much, like we took sections, it wasnt like we worked on all the sections together by sharing screens/ logc. but we did wal keach other through what we did the next day and expalined our logic. not sure which approach is best... 
> I wasnt sure how to set up the repo stuff but my partner has more experisnce using is becaues hes going for a master in computer scinece and was well versed. that was great to have someone with experince with this. my only exposure has been this clas... 

I think we made a good team. we tried to meet before HW6 was due, the exam, and over fall break. We were good at reaching out and starting a conversation. 

I always wish i have more time. but i think we did a good job with the time we had.


    
 
  


.: *Links:* :.

[Main Page of Blog Posts Link](https://magarittenguyen.github.io/)
 
[Project 2 Blog Post Link](https://magarittenguyen.github.io/2022/10/12/STT558-project2-group2c-blog-post.html)

[Vingette Link](https://pages.github.ncsu.edu/sdharma2/ST558_Project_2_C/)

[Project 2 GitHub Repo Link](https://github.ncsu.edu/sdharma2/ST558_Project_2_C)

[HTML Link of Vignette](https://magarittenguyen.github.io/README.html)


Thank you!
