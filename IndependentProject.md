Florida Manatee Abundance Estimates using Satellite Imagery
================
Kirby Parnell
2019-06-10

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

Preliminary Notes and Plan
--------------------------

-   Florida stock includes four regional management units ![Florida manatee distribution within the four designated regional management units. USFWS (2001).](Manatee%20Regional%20Unit.png)

-   "Updated Statewide Abundance Estimates for the Florida Manatee, Technical Report 2018" ![Baseline abundance estimates (with 95% credible intervals and coefficient of variation) by region and survey. Estimates and 95% CRI are rounded to the nearest 10.](FL%20manatee%20abundance%20estimate.png)

-   Potential Locations: King Spring, Three Sisters Spring on Crystal River, Ten Thousand Islands, Haulover Canal Manatee Viewing Area, Blue Spring State Park

-   Criteria to maximize satellite images: which location is best, how often manatees are there? Near big city? We want temporal consistency, as many images we can get from same location and same date every year

-   How many nice images can we get for each of these locations 1. during manatee season and 2. during off-season?

-   Should each area be the same size?

Summary
-------

Is satellite imagery a viable option to estimate the Florida manatee abandunce? How do counts of manatees from satellite imagery compare to that of traditional aerial surveys?

Question(s)
-----------

-   Question 1: How do manatee counts from satellite imagery compare to traditional aerial survey counts from two manatee hotspots in King's Bay, Crystal River, FL?

Introduction
------------

Manatee estimates are difficult to obtain due to their widespread and changing distribution throughout Florida and the limitations of aerial surveys. Satellite imagery is potentially a new tool to estimate manatee abundance and track temporal and spatial changes.

Methods
-------

-   I will look at Kings Bay, Crystal River area because I found this statement online, "Florida manatee (present in Kings Bay and Crystal River NWR year-round, but highest aggregation November – March = approx. 600 manatees vs. summer months = approx. 30 manatees)." Now I have a number to compare my counts from satellites to. See this information at <https://www.fws.gov/refuge/crystal_river/wildlife_and_habitat/florida_manatee.html>

-   Manatee Sancuaries are in effect from November 15 to March 31. ![Map of King's Bay, Crystal River, Florida](King's%20Bay%20map.png)

-   I will count manatees in Google Earth Pro near King Spring (\#10 on the map) and Idiot's Delight (\#9 on the map).

-   Tag each animal in Google Earth Pro

1.  **Google Earth Protocol adapted from Liz's Module**
    -   I need to ask Liz where to find the document that shows the resolution and satellite for each date I use
    -   Use the Time Slider to select the dates’ you want to count manatees:

        | Date (yyyymmdd) | Resolution (m) | Satellite                             | Provider     |
        |-----------------|----------------|---------------------------------------|--------------|
        | 20130115        | 0.15           | NA; aerial imagery                    | Unknown      |
        | 20130822        | 0.50           | WorldView-1/2, GeoEye-1, or Quickbird | DigitalGlobe |
        | 20110108        | ~1.00          | Ikonos                                | DigitalGlobe |
        | 20030412        | ~2.00          | EarlyBird-1 (?)                       | DigitalGlobe |

    -   Use the polygon measurement tool to extract area/perimeter
    -   Manually copy measurements into excel file
    -   Tag each manatee using the Add Placemark option
    -   Drag saved placemarks to My Places
    -   Frequently save My Places (File -&gt; Save -&gt; Save My Places)
    -   *Note*: if you need to go back to measurements, right-click on outlines (or their corresponding saved names in My Places) -&gt;

-   Create an excel spreadsheet with the column titles: location (King or ID), date of image, image resolution, satellite, number of individuals, defined area size (should be the same for all analyses)

-   Compare results to the above statement and hopefully to more detailed counts that I will find online.

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

Literature and Website Sources
------------------------------

-   "Updated Statewide Abundance Estimates for the Florida Manatee" Technical Report No. 23, 2018; JEFFREY A. HOSTETLER, HOLLY H. EDWARDS, JULIEN MARTIN, AND PAUL SCHUELLER <https://f50006a.eos-intl.net/ELIBSQL12_F50006A_Documents/TR23-18Hostetler-USAEF.pdf>

-   “New Aerial Survey and Hierarchical Model to Estimate Manatee Abundance”

-   Status and threats analysis for the Florida manatee (Trichechus manatus latirostris), 2016, Scientific Investigations Report 2017-5030

-   U.S. Fish and Wildlife Service West Indian Manatee Florida Stock SAR <https://www.fws.gov/ecological-services/es-library/pdfs/West-Indian-Manatee-FL-Final-SAR.pdf>

-   "Combining information for monitoring at large spatial scales: first statewide abundance estimate of the Florida manatee" Biological Conservation 186 (2015) 44–51.
