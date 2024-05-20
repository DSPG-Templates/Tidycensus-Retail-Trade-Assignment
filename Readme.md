## Activity Goal

The goal of this activity will be to demonstrate your ability to work
with the `tidycensus` API to pull data from the US Census Bureau and to
meaningful represent the data using R's visualization libraries.

## Requirements

Students should;

-   Go through the `tidycensus` training material
-   Have completed the first Retail Trade Exercise
-   Have some familiarity with the `ggplot2` and `dplyr` packages
    -   Packages covered in the [R for Data
        Science](https://r4ds.hadley.nz/) book
-   Have used the [R Graphics Cookbook](https://r-graphics.org/) or
    [Elegant Graphics for Data Analysis](https://ggplot2-book.org/)
-   Have used the quarto markdown system for creating blogs

## Assignment Details

This activity will build off of the Retail Trade Exercise. Students will
be using the [Census Reporter](https://censusreporter.org/topics/) to
identify tables that will further inform their questions posed in the
Retail Trade Exercise.

For example, a group that originally looked at prison data may want look
at census tables relating to Education, Poverty, Population, Employment
or Group Quarters. The choice of data tables is left to the decision of
the groups based on the questions they plan to answer.

The goal is for students to get a chance to revisit their Retail Trade
work and make amendments based on the reviews from their presentations
and to add onto their work by using data from the US Census.

The final presentation of the material students come up with will be
presented through a quarto markdown document, which they've learned to
use through training on their personal blogs. This is the
`Tidycensus_Assignment.qmd` file.

## Structure of Repository

### Data

The `Data` folder should contain all of the data that is used to make
any form of analysis. In this case, the folder will contain the Retail
Trade data sets and any of the data sets that are retrieved using the
`tidycensus` API.

Data from `tidycensus` should be saved in the `.RDS` format. The
following code saves a data object called `df` as an `.RDS` file and
loads the file again.

``` r
# Save file
saveRDS(df, file = "Data/Median_Age_2022.RDS")

# Read file
df <- readRDS(file = "Data/Median_Age_2022.RDS")

# Functions to read excel files include
read.csv() # Reads in csv format
readxl::read_excel() # Reads in xlsx format
```

### Images

Any images of graphics you produce should be placed in the `imgs`
directory. This includes figures made in R that will be part of the
final presentation.

## Code Chunk Settings

Since the data sets will be saved in the `Data` folder, there is no need
to run code where a census API call is being made in the submission. For
this reason, any of the API call code chunks should be set to
`eval=FALSE`. You should include the code itself, but not execute the
code. Instead load the data set from the saved `.RDS` file

## Software

In the Retail Trade Exercise, you were given the opportunity to work
with any software, for this exercise, the goal will be to try and
complete the graphics and data manipulation in R as much as possible.
The `tidycensus` API is tightly integrated with R's packages so this is
intended to make the workflow easier.

## Submission Details

When submitting the assignment, make sure that the metadata information
is correctly attributed and that the code runs for all members of the
group. The final deliverable will include the following.

-   Code used while working with the data
-   Data sets in the appropriate forms in the `Data` directory
-   Images generated while working on the assignment
-   A final presentation of the material using a quarto markdown
    document
    -   This file should be renamed to
        `GroupNumber_Tidycensus_Assignment.qmd` where `GroupNumber` is
        `GroupOne` or `GroupTwo` etc.
