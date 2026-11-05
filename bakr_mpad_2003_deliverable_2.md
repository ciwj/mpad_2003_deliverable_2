**Date**: Nov. 5, 2026<br>
**Course Code & Course Name**: MPAD 2003 - Introductory Data Storytelling<br>
**Student's First Name & Last Name**: Zahira Bakr<br>
**Presented to Jean-Sébastien Marier**<br>

# Deliverable 2: Exploratory Data Analysis (EDA)

Use one hashtag symbol (`#`) to create a level 1 heading like this one.

## Foreword

For this assignment, you must clean and analyze the dataset from Deliverable 1, create exploratory charts/visualizations, and identify a potential story. Your assignment must clearly detail your process. You are expected to write about 1,000-1,200 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub.

I have been assigning different versions of this project to my digital journalism and data storytelling students for a few years now. Its structure was inspired by the main sections/chapters of [*The Data Journalism Handbook*](https://datajournalism.com/read/handbook/one/). This version was further inspired by the [Key Capabilities in Data Science](https://extendedlearning.ubc.ca/programs/key-capabilities-data-science) program offered by the University of British Columbia (UBC).

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## 1. Getting Data

Use two hashtag symbols (`##`) to create a level 2 heading like this one.

To include a screen capture, use the sample code below. Your images should be saved in the same folder as your `.md` file.

![](import-screen-capture.png)<br>
*Figure 1: The "Import file" prompt on Google Sheets.*

**Here are examples of functions and lines of code put in grey boxes:**

1. If you name a function, put it between "angled" quotation marks like this: `IMPORTHTML`.
1. If you want to include the entire line of code, do the same thing, albeit with your entire code: `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternatively, you can put your code in an independent box using the template below:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
This also shows how to create an ordered list. Simply put `1.` before each item.

All data was sourced from the Ottawa Neighbourhood Study (ONS-SQO). To gather the data from their [website](https://ons-sqo.ca/maps/), the chart visualization for a given dataset was selected. HTML sources were downloaded from the page, and the data table manually selected. This is because the data takes the form of an interactive visualization with options between map and chart views, and as such Google Sheets was not able to import the embedded HTML table. 
Once the HTML table was isolated it was compiled on a dedicated web page found at [this page](https://oughegr.neocities.org/), to then be imported using Sheets' `=IMPORTHTML("https://oughegr.neocities.org/", "table", n)`, where `n` was 1-23.

The resulting data can be found [here](https://docs.google.com/spreadsheets/d/1LsJBjsZ38paX0MrHKggheRsNlp18-JJRSkHBtGmfKiQ/edit?usp=sharing).

## 2. Understanding Data

### 2.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

Insert text here.

Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As seen in Bounegru & Gray (2011), a data visualization should be clear...

### 2.2. Cleaning Data

Several neighbourhoods were excluded due to an absence of data - the original datasets exclude several, such as Carleton University and Beechwood Cemetary, due to not having reliable data in those communities. At this point, the list of communities are:

Ottawa

Alta Vista

Bayshore

Beacon Hill South - Cardinal Heights

Beaverbrook

Bells Corners East

Bells Corners West

Billings Bridge - Heron Park

Blackburn Hamlet

Blossom Park - Timbermill

Borden Farm - Fisher Glen

Braemar Park - Bel Air Heights - Copeland Park

Bridlewood - Emerald Meadows

Britannia

Brookside - Briarbrook - Morgan's Grant

Cardinal Creek

Carleton Heights - Courtland Park

Carlington

Carp

Carson Grove - Carson Meadows

Centrepointe

Centretown

Chapel Hill North

Chapel Hill South

Chapman Mills

City view

Civic Hospital

Constance Bay

Convent Glen - Orléans Woods

Corkery

Craig Henry - Manordale

Crestview - Tanglewood

Crystal Bay - Lakeview Park

Cumberland

Dunrobin

Edwards - Carlsbad Springs

Elmvale - Canterbury

Emerald Woods - Sawmill Creek

Fallingbrook

Findlay Creek

Fisher Heights

Fitzroy

Glebe - Dows Lake

Glen Cairn

Greely

Greenboro East

Greenboro West

Hawthorne Meadows - Sheffield Glen

Hintonburg - Mechanicsville

Hunt Club Park

Iris

Island Park - Wellington Village

Kanata Lakes

Katimavik - Hazeldean

Kinburn

Laurentian

Ledbury - Heron Gate - Ridgemont

Leslie Park - Bruce Farm

Lowertown East

Lowertown West

Manor Park

Manotick

Marlborough

Merivale Gardens - Grenfell Glen - Pineglen - Country Place

Metcalfe

Munster - Ashton

Navan - Sarsfield

New Edinburgh

North Gower - Kars

Old Barrhaven East

Old Barrhaven West

Old Hunt Club

Old Ottawa East

Old Ottawa South

Orléans Village - Chateauneuf

Osgoode - Vernon

Overbrook

Parkwood Hills

Pineview

Playfair Park - Guildwood Estates

Portobello South

Qualicum - Redwood

Queensway Terrace North

Queenswood - Chatelaine

Queenswood Heights

Richmond

Rideau Crest - Davidson Heights

Riverside Park - Mooney's Bay

Riverside Park South - Revelstoke

Riverside South - Leitrim

Riverview

Rockcliffe Park

Rothwell Heights - Beacon Hill North

Sandy Hill

South Keys

Stittsville

Stittsville East

Stittsville North

Stonebridge - Half Moon Bay

Trend-Arlington

Vanier North

Vanier South

Vars

Wateridge Village

West Centretown

Westboro

Whitehaven - Woodpark - Glabar Park

### 2.3. Analyzing Data

| CORRELATION                                                                                         | Total population (2021) | Average after-tax income among recipients (2020, $) | Low-income prevalence (LIM-AT, total population, %) | 2021 SES Quintiles | % renter households | % of households in core housing need | % Total racialized population (2021) | % immigrants | % recent immigrants (arrived 2016-2021) | % refugees | Emergency department visits: all (age-standardized rate per 1,000 residents, age 0+ years) | Emergency department visits: high urgency (age-standardized rate per 1,000 residents, age 0+ years) | Emergency department visits: low urgency (age-standardized rate per 1,000 residents, age 0+ years) | Mental health visits to primary care (age-standardized rate per 100 residents, age 20+ years) | % attached to a primary care provider | % uncertainly attached to a primary care provider | 2+ common chronic conditions (age-standardized rate per 100 residents, age 20+ years) | 4+ chronic conditions (age-standardized rate per 100 residents, age 0+ years) | Voter turnout (%, 2022 municipal election) | Total Criminal Code offences (per 1000, plus 50m buffer) | Total crimes against property (per 1000, plus 50m buffer) | Total crimes against the person (per 1000, plus 50m buffer) | Total other crimes (per 1000, plus 50m buffer) |
|-----------------------------------------------------------------------------------------------------|-------------------------|-----------------------------------------------------|-----------------------------------------------------|--------------------|---------------------|--------------------------------------|--------------------------------------|--------------|-----------------------------------------|------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|---------------------------------------|---------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|-----------------------------------------------------------|-------------------------------------------------------------|------------------------------------------------|
| Total population (2021)                                                                             |                       1 |                                               -0.01 |                                                   0 |              -0.08 |                0.03 |                                 0.01 |                                 0.05 |         0.04 |                                    0.02 |       0.01 |                                                                                      -0.01 |                                                                                               -0.01 |                                                                                              -0.01 |                                                                                         -0.01 |                                 -0.02 |                                              0.02 |                                                                                 -0.01 |                                                                         -0.02 |                                      -0.02 |                                                        0 |                                                         0 |                                                           0 |                                              0 |
| Average after-tax income among recipients (2020, $)                                                 |                   -0.01 |                                                   1 |                                               -0.53 |              -0.72 |               -0.45 |                                -0.62 |                                -0.45 |        -0.38 |                                   -0.52 |      -0.59 |                                                                                      -0.39 |                                                                                               -0.43 |                                                                                              -0.19 |                                                                                         -0.17 |                                  0.42 |                                             -0.42 |                                                                                 -0.66 |                                                                         -0.21 |                                       0.59 |                                                    -0.17 |                                                     -0.17 |                                                       -0.21 |                                          -0.04 |
| Low-income prevalence (LIM-AT, total population, %)                                                 |                       0 |                                               -0.53 |                                                   1 |               0.79 |                0.92 |                                 0.92 |                                 0.51 |         0.47 |                                    0.63 |       0.69 |                                                                                       0.43 |                                                                                                0.52 |                                                                                               0.12 |                                                                                          0.06 |                                 -0.89 |                                              0.89 |                                                                                  0.27 |                                                                          0.29 |                                      -0.51 |                                                     0.53 |                                                      0.51 |                                                        0.55 |                                           0.01 |
| 2021 SES Quintiles                                                                                  |                   -0.08 |                                               -0.72 |                                                0.79 |                  1 |                0.72 |                                 0.83 |                                 0.53 |         0.51 |                                    0.59 |       0.68 |                                                                                       0.37 |                                                                                                0.48 |                                                                                               0.05 |                                                                                          0.21 |                                 -0.71 |                                              0.71 |                                                                                  0.51 |                                                                          0.35 |                                      -0.54 |                                                     0.36 |                                                      0.35 |                                                        0.39 |                                          -0.07 |
| % renter households                                                                                 |                    0.03 |                                               -0.45 |                                                0.92 |               0.72 |                   1 |                                 0.89 |                                  0.5 |         0.48 |                                    0.62 |       0.62 |                                                                                       0.33 |                                                                                                0.44 |                                                                                                  0 |                                                                                          0.12 |                                 -0.93 |                                              0.93 |                                                                                  0.18 |                                                                          0.34 |                                      -0.38 |                                                     0.54 |                                                      0.52 |                                                        0.55 |                                              0 |
| % of households in core housing need                                                                |                    0.01 |                                               -0.62 |                                                0.92 |               0.83 |                0.89 |                                    1 |                                 0.52 |         0.51 |                                    0.73 |       0.76 |                                                                                       0.36 |                                                                                                0.45 |                                                                                               0.08 |                                                                                           0.1 |                                 -0.83 |                                              0.83 |                                                                                  0.39 |                                                                          0.29 |                                      -0.51 |                                                     0.39 |                                                      0.38 |                                                        0.42 |                                           0.02 |
| % Total racialized population (2021)                                                                |                    0.05 |                                               -0.45 |                                                0.51 |               0.53 |                 0.5 |                                 0.52 |                                    1 |         0.96 |                                    0.78 |       0.81 |                                                                                       0.03 |                                                                                                0.12 |                                                                                              -0.18 |                                                                                          -0.2 |                                 -0.56 |                                              0.56 |                                                                                  0.19 |                                                                          0.02 |                                      -0.65 |                                                     0.12 |                                                      0.12 |                                                        0.15 |                                          -0.03 |
| % immigrants                                                                                        |                    0.04 |                                               -0.38 |                                                0.47 |               0.51 |                0.48 |                                 0.51 |                                 0.96 |            1 |                                    0.79 |        0.8 |                                                                                      -0.01 |                                                                                                0.08 |                                                                                               -0.2 |                                                                                         -0.18 |                                 -0.52 |                                              0.52 |                                                                                  0.15 |                                                                          0.03 |                                      -0.57 |                                                     0.09 |                                                      0.09 |                                                        0.11 |                                          -0.06 |
| % recent immigrants (arrived 2016-2021)                                                             |                    0.02 |                                               -0.52 |                                                0.63 |               0.59 |                0.62 |                                 0.73 |                                 0.78 |         0.79 |                                       1 |       0.86 |                                                                                       0.17 |                                                                                                0.23 |                                                                                                  0 |                                                                                         -0.21 |                                 -0.63 |                                              0.63 |                                                                                  0.27 |                                                                          0.09 |                                      -0.53 |                                                     0.16 |                                                      0.17 |                                                        0.16 |                                          -0.01 |
| % refugees                                                                                          |                    0.01 |                                               -0.59 |                                                0.69 |               0.68 |                0.62 |                                 0.76 |                                 0.81 |          0.8 |                                    0.86 |          1 |                                                                                       0.19 |                                                                                                0.27 |                                                                                              -0.03 |                                                                                         -0.06 |                                  -0.6 |                                               0.6 |                                                                                   0.4 |                                                                          0.08 |                                      -0.65 |                                                     0.11 |                                                       0.1 |                                                        0.17 |                                          -0.01 |
| Emergency department visits: all (age-standardized rate per 1,000 residents, age 0+ years)          |                   -0.01 |                                               -0.39 |                                                0.43 |               0.37 |                0.33 |                                 0.36 |                                 0.03 |        -0.01 |                                    0.17 |       0.19 |                                                                                          1 |                                                                                                0.96 |                                                                                               0.82 |                                                                                          0.04 |                                 -0.33 |                                              0.33 |                                                                                  0.49 |                                                                          0.48 |                                      -0.37 |                                                     0.31 |                                                      0.29 |                                                        0.41 |                                           0.07 |
| Emergency department visits: high urgency (age-standardized rate per 1,000 residents, age 0+ years) |                   -0.01 |                                               -0.43 |                                                0.52 |               0.48 |                0.44 |                                 0.45 |                                 0.12 |         0.08 |                                    0.23 |       0.27 |                                                                                       0.96 |                                                                                                   1 |                                                                                               0.62 |                                                                                          0.17 |                                 -0.45 |                                              0.45 |                                                                                  0.57 |                                                                          0.62 |                                      -0.44 |                                                     0.38 |                                                      0.36 |                                                        0.49 |                                           0.06 |
| Emergency department visits: low urgency (age-standardized rate per 1,000 residents, age 0+ years)  |                   -0.01 |                                               -0.19 |                                                0.12 |               0.05 |                   0 |                                 0.08 |                                -0.18 |         -0.2 |                                       0 |      -0.03 |                                                                                       0.82 |                                                                                                0.62 |                                                                                                  1 |                                                                                         -0.24 |                                     0 |                                                 0 |                                                                                  0.19 |                                                                          0.06 |                                      -0.12 |                                                     0.07 |                                                      0.07 |                                                        0.13 |                                           0.06 |
| Mental health visits to primary care (age-standardized rate per 100 residents, age 20+ years)       |                   -0.01 |                                               -0.17 |                                                0.06 |               0.21 |                0.12 |                                  0.1 |                                 -0.2 |        -0.18 |                                   -0.21 |      -0.06 |                                                                                       0.04 |                                                                                                0.17 |                                                                                              -0.24 |                                                                                             1 |                                 -0.06 |                                              0.06 |                                                                                  0.33 |                                                                          0.39 |                                       0.09 |                                                     0.13 |                                                      0.13 |                                                        0.15 |                                          -0.04 |
| % attached to a primary care provider                                                               |                   -0.02 |                                                0.42 |                                               -0.89 |              -0.71 |               -0.93 |                                -0.83 |                                -0.56 |        -0.52 |                                   -0.63 |       -0.6 |                                                                                      -0.33 |                                                                                               -0.45 |                                                                                                  0 |                                                                                         -0.06 |                                     1 |                                                -1 |                                                                                 -0.14 |                                                                         -0.31 |                                       0.41 |                                                    -0.62 |                                                      -0.6 |                                                       -0.63 |                                              0 |
| % uncertainly attached to a primary care provider                                                   |                    0.02 |                                               -0.42 |                                                0.89 |               0.71 |                0.93 |                                 0.83 |                                 0.56 |         0.52 |                                    0.63 |        0.6 |                                                                                       0.33 |                                                                                                0.45 |                                                                                                  0 |                                                                                          0.06 |                                    -1 |                                                 1 |                                                                                  0.14 |                                                                          0.31 |                                      -0.41 |                                                     0.62 |                                                       0.6 |                                                        0.63 |                                              0 |
| 2+ common chronic conditions (age-standardized rate per 100 residents, age 20+ years)               |                   -0.01 |                                               -0.66 |                                                0.27 |               0.51 |                0.18 |                                 0.39 |                                 0.19 |         0.15 |                                    0.27 |        0.4 |                                                                                       0.49 |                                                                                                0.57 |                                                                                               0.19 |                                                                                          0.33 |                                 -0.14 |                                              0.14 |                                                                                     1 |                                                                          0.55 |                                      -0.57 |                                                    -0.03 |                                                     -0.04 |                                                        0.08 |                                          -0.03 |
| 4+ chronic conditions (age-standardized rate per 100 residents, age 0+ years)                       |                   -0.02 |                                               -0.21 |                                                0.29 |               0.35 |                0.34 |                                 0.29 |                                 0.02 |         0.03 |                                    0.09 |       0.08 |                                                                                       0.48 |                                                                                                0.62 |                                                                                               0.06 |                                                                                          0.39 |                                 -0.31 |                                              0.31 |                                                                                  0.55 |                                                                             1 |                                      -0.15 |                                                     0.31 |                                                      0.31 |                                                        0.31 |                                          -0.03 |
| Voter turnout (%, 2022 municipal election)                                                          |                   -0.02 |                                                0.59 |                                               -0.51 |              -0.54 |               -0.38 |                                -0.51 |                                -0.65 |        -0.57 |                                   -0.53 |      -0.65 |                                                                                      -0.37 |                                                                                               -0.44 |                                                                                              -0.12 |                                                                                          0.09 |                                  0.41 |                                             -0.41 |                                                                                 -0.57 |                                                                         -0.15 |                                          1 |                                                    -0.18 |                                                     -0.17 |                                                       -0.25 |                                          -0.08 |
| Total Criminal Code offences (per 1000, plus 50m buffer)                                            |                       0 |                                               -0.17 |                                                0.53 |               0.36 |                0.54 |                                 0.39 |                                 0.12 |         0.09 |                                    0.16 |       0.11 |                                                                                       0.31 |                                                                                                0.38 |                                                                                               0.07 |                                                                                          0.13 |                                 -0.62 |                                              0.62 |                                                                                 -0.03 |                                                                          0.31 |                                      -0.18 |                                                        1 |                                                      0.99 |                                                         0.9 |                                           0.02 |
| Total crimes against property (per 1000, plus 50m buffer)                                           |                       0 |                                               -0.17 |                                                0.51 |               0.35 |                0.52 |                                 0.38 |                                 0.12 |         0.09 |                                    0.17 |        0.1 |                                                                                       0.29 |                                                                                                0.36 |                                                                                               0.07 |                                                                                          0.13 |                                  -0.6 |                                               0.6 |                                                                                 -0.04 |                                                                          0.31 |                                      -0.17 |                                                     0.99 |                                                         1 |                                                        0.86 |                                           0.03 |
| Total crimes against the person (per 1000, plus 50m buffer)                                         |                       0 |                                               -0.21 |                                                0.55 |               0.39 |                0.55 |                                 0.42 |                                 0.15 |         0.11 |                                    0.16 |       0.17 |                                                                                       0.41 |                                                                                                0.49 |                                                                                               0.13 |                                                                                          0.15 |                                 -0.63 |                                              0.63 |                                                                                  0.08 |                                                                          0.31 |                                      -0.25 |                                                      0.9 |                                                      0.86 |                                                           1 |                                          -0.01 |
| Total other crimes (per 1000, plus 50m buffer)                                                      |                       0 |                                               -0.04 |                                                0.01 |              -0.07 |                   0 |                                 0.02 |                                -0.03 |        -0.06 |                                   -0.01 |      -0.01 |                                                                                       0.07 |                                                                                                0.06 |                                                                                               0.06 |                                                                                         -0.04 |                                     0 |                                                 0 |                                                                                 -0.03 |                                                                         -0.03 |                                      -0.08 |                                                     0.02 |                                                      0.03 |                                                       -0.01 |                                              1 |

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 3. Delivering Data

Insert text here.

## 4. References

Include a list of your references here. Please follow [APA](https://apastyle.apa.org/style-grammar-guidelines/references) or [MLA](https://www.mla.org/MLA-Style) guidelines for references. Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
