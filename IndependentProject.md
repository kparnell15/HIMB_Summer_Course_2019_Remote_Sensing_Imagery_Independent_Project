HIMB Summer Course Independent Project
================
INSERT YOUR NAME
2019-05-31

R Markdown information
----------------------

(remove this section once you no longer need this information)

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button, a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

``` r
summary(cars)
```

    ##      speed           dist       
    ##  Min.   : 4.0   Min.   :  2.00  
    ##  1st Qu.:12.0   1st Qu.: 26.00  
    ##  Median :15.0   Median : 36.00  
    ##  Mean   :15.4   Mean   : 42.98  
    ##  3rd Qu.:19.0   3rd Qu.: 56.00  
    ##  Max.   :25.0   Max.   :120.00

Try pressing the **Knit** button now to see what this looks like.

Here is a 'cheat sheet' for how to format text in RMarkdown (e.g., how to make headings, bold text, italics, bulleted/numbered lists, etc.):

<https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf>

Summary
-------

Insert here a brief (1-2 sentence) summary of your project. This section will eventually become your abstract.

Question(s)
-----------

Insert here the specific, testable question(s) your project seeks to answer.

-   Question 1:
-   Question 2:
-   etc.

Introduction
------------

Insert here some brief (2-3 sentence) background information on your project (e.g., what the current state of knowledge is on the topic, why your question(s) need to be answered, etc.).

Methods
-------

Insert here a few sentences and/or dot points to briefly summarize the methods you're using. Include any details you'd need to know if coming back to this project at a later date when you might not remember exactly what you did this week.

You can embed images (e.g., maps, diagrams, screenshots, etc.) by using the following code:

Images on the web:

![optional caption text](https://www.bestfunnies.com/wp-content/uploads/2012/08/Funny-Fish-11.jpg)

To add images from your local files that are stored in the same directory (folder) as your Rproject, replace the web address above with the fliename of your image.

Results
-------

Summarize the current status of the project - i.e., how far you got in your data collection, what's left to do, any patterns you've noticed so far. etc.

Once you've collected your data, this is where you'll do your R plotting and analyses.

You can embed plots in this section, for example (replace this with your own when you're ready to make plots):

![](IndependentProject_files/figure-markdown_github/pressure%20plot-1.png)

(Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot, but this can be changed if, for example, you want to share both your code and your plots with collaborators in early stages of a manuscript.)

You would also do your analyses in this section, and you can choose whether or not your code and analytical results show up in the output (knitted) document, for example (replace this with your own when you're ready to do analyses):

``` r
model <- lm(pressure~temperature, data = pressure)
summary(model)
```

    ## 
    ## Call:
    ## lm(formula = pressure ~ temperature, data = pressure)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -158.08 -117.06  -32.84   72.30  409.43 
    ## 
    ## Coefficients:
    ##              Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept) -147.8989    66.5529  -2.222 0.040124 *  
    ## temperature    1.5124     0.3158   4.788 0.000171 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 150.8 on 17 degrees of freedom
    ## Multiple R-squared:  0.5742, Adjusted R-squared:  0.5492 
    ## F-statistic: 22.93 on 1 and 17 DF,  p-value: 0.000171

Discussion
----------

insert here a few sentences about anything you've learned so far - e.g., any unexpected patterns, any challenges you've had, next steps, etc.

References
----------

You won't likely need this section at this stage, but when you're writing a paper, can insert references into RMardown docs - see <https://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html>.
