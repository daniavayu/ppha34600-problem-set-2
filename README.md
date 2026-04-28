# PPHA 34600: Program Evaluation

Spring 2026

## Problem Set 2

**Due:** Friday, May 1, at 11:59PM Chicago time to Gradescope via Canvas

## Instructions

This problem set consists of two files: (1) this document with instructions and questions; and (2) a dataset which you will use to answer the questions below.

You can work in groups of up to three. Please include your name along with your group members' names on your submission. You should submit both written answers -- which should be parsimonious -- and your code and results for the data analysis as one single PDF document.

You may use any programming language (e.g., R, Python, etc.), but this course will provide support only in R, including during TA sessions, office hours and in the provided solutions. If you use R, we recommend that you use RMarkdown or knitr, which will allow you to intersperse your code and written answers (but this is not required). Note that you are primarily being graded on your written answers. Problem sets must be submitted in PDF format. Problem sets must be turned in Gradescope via Canvas.

Your written solution (not including code) to each problem should not exceed 250 words.

If this problem set is submitted late, your late token will automatically be used. Do not email us to ask for your late token to be used. If you have already used your late token, you will receive a zero for a late submission.

## Questions

1. PEDAP are interested in answering the following question: What is the average effect of grid electricity connection on firm annual revenues (measured in USD)? To make sure everybody is on the same page, explain to them what the ideal experiment would be for answering this question. Next, use math (the potential outcomes framework) and words to explain what you would estimate and how you would do so. Make sure to be clear about the unit of analysis (i.e., what is "i" here?). Word limit: 250 words.

2. PEDAP has some data available, and they believe they can compare firms that are connected to the grid, to those who aren't. They make a dataset available to you, in the form of `ps3_data_Spring26.csv`. Explain what you would recover if you simply compared connected to non-connected firms. Produce a balance table which displays the differences on observable characteristics between firms that are connected to the grid versus those that are not connected. Interpret this table. Does this table give you more or less faith in the comparison PEDAP would like to make? Word limit: 250 words.

3. (Optional, ungraded question) PEDAP acknowledges that a simple comparison may not work, but they still want an estimate of the impacts of being connected to the grid. PEDAP's CEO recently took a class on impact evaluation and learned about selection-on-observables designs. They have asked you to apply this methodology. Use a regression-based approach to estimate the effect of the grid-connection on firm revenue. Interpret your results. What are the strengths and weaknesses of this approach? How do your results differ from what you find if you instead use the naive estimator? Word limit: 250 words.

4. Use an exact matching approach to estimate the effect of a grid connection on firm revenue. What variables did you decide to include in the matching procedure (remember you don't have to use all the variables at your disposal)? Interpret your results. What are the strengths and weaknesses of this approach? How do your results differ from what you find if you use the naive estimator? Did you run into the Curse of Dimensionality with this analysis? If yes, describe how it affected your approach. If not, describe how the Curse could have generated problems in this setting. Word limit: 250 words.

5. PEDAP has decided they are not interested in using a selection-on-observables approach after your discussions with them. Instead, they mention that they have also heard about a strategy called instrumental variables (IV) and are considering using land gradient as an instrument. They would like you to discuss the plausibility of this instrument and outline its limitations. They would also like you to propose an alternative instrumental variable that could be used to evaluate the effect of grid electricity connection on firm revenues. Why would your proposed instrument be a good one? Do you have any concerns about your ability to estimate the treatment effect using your instrument? If so, explain why; if not, explain why not. Word limit: 250 words.

6. PEDAP is convinced that this approach is the most feasible given their data limitations. After an internal discussion, they've come back to you with great news! It turns out that one of the many well-meaning development economists at the University of Chicago ran a small pilot program where they randomly offered a grid connection subsidy (covering hookup fees and initial wiring costs) to some firms as part of an attempt to publish a paper in the American Economic Review (it is still unpublished). With this new information, please explain how you would use the subsidy program to estimate the impact of actually connecting to the grid on firm revenues. Use both words and math. Word limit: 250 words.

7. PEDAP agree that your approach is a good one. So good, in fact, that they'd like to see it in action! They forgot to tell you that the dataset they provided you will allow you to apply this approach as well. Please report the results of a regression that recovers the impact of grid connection subsidies on the take-up of grid electricity by a firm, using `grid_subsidy_amount` as the subsidy variable (note that this pilot randomly gave different subsidy amounts to different firms -- this is not just a binary variable) and `grid_connection` as an indicator for having successfully connected to the national electricity grid. What parameter does this estimate? Interpret your estimate. Word limit: 250 words.

8. PEDAP want you to use the pilot for the next steps of your analysis (they are ignoring any opinion you gave in (5), good or bad - welcome to the real world). They'd first like to learn a little bit more about the pilot itself: they want you to use a regression to estimate the effects of the grid connection subsidies (using `grid_subsidy_amount`) on firm annual revenues (`firm_revenue`). What parameter does this regression estimate? Interpret your estimate. Is it useful for policy? Why or why not? Word limit: 250 words.

9. Finally, PEDAP wants you to use the pilot to estimate the impacts of grid electricity connection on firm revenues. For full transparency, make sure to show all of your analysis steps. PEDAP cares about your standard errors here, so be sure to get them right. Interpret your results: Does grid electricity connection matter for firm revenues? Word limit: 250 words.

10. PEDAP like your analysis and are now intrigued by using the subsidy as a policy tool. But they're a bit worried about the quality of their data. While the firm revenue survey data were of extremely high quality, but the pilot research team did not keep great records of the subsidy amounts that were disbursed to firms. The development economist describes two possibilities and wants your opinion. First, she wants to know if it would be a problem for your analysis -- looking at the causal effect of the subsidy on firm revenues -- if the subsidy amount data included random noise? Why or why not? If yes, can you use an instrumental variables approach to address this problem? Second, she wants to know if it would be a problem for your analysis if larger subsidy amounts were recorded with error, but smaller subsidy amounts were accurately recorded. If yes, can you use an instrumental variables approach to address this problem? Word limit: 250 words.
