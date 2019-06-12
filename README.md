# Success on Kickstarter

Over two billion dollars have been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Only a third of the over 300,000 projects launched on Kickstarter have made it through the funding process with a positive outcome.

Since getting funded on Kickstarter requires meeting or exceeding the project's initial goal, many organizations spend months looking through past projects in an attempt to discover some trick to finding success.

## What This Is:

An analysis of data on four thousand past Kickstarter projects in order to discover successful project trends.

## Program Used:

Excel

## How This Was Done:

* Conditional formatting was done on the `state` column with a corresponding color for each campaign state:
    * "successful" - light green
    * "failed" - red
    * "cancelled" - yellow
    * "currently live" - dark green

* Created a `percent funded` column that calculates the amount of money a campaign made towards reaching its initial goal.

* Used conditional formatting for the `percent funded` column, with 0 values starting at red, values at 100 transitition to a green, and values approaching 200 transitioning to a light blue.

* Created a new column called `average donation`, which used a formula to calculate how much each backer paid on average.

* Created colums `category` and `sub-category` to store the split contents of the `Category and Sub-Category` column 

* Created a  pivot table in a new sheet that analyzed how many campaigns were "successful", "failed," "cancelled," or are currently "live" per category. 
    * Created a stacked column pivot chart that can be filtered by `country`.

* Created a  pivot table in a new sheet that analyzed how many campaigns were "successful", "failed," "cancelled," or are currently "live" per sub-category. 
    * Created a stacked column pivot chart that can be filtered by `country` and `parent-category`.

* The dates within the `deadline` and `launched_at` columns were converted into normal date format from unix timestap in two new columns: `Date Ended Conversion` and `Date Created Conversion`. 

* Created a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.
    * Created a pivot chart line graph.

* Created a new sheet with 8 columns: `Goal`, `Number Successful`, `Number Failed`, `Number Canceled`, `Total Projects`, `Percentage Successful`, `Percentage Failed`, and `Percentage Canceled`
    * Counted how many successful, failed, and canceled projects were created within certain goals that were set
    * Found the percentage of projects which were successful, failed, or were canceled per goal range


LINK TO CONCLUSIONS FROM THE KICKSTARTER DATA: [Conclusions](Conclusions.txt)


