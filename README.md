# Stanford Open Policing Project:   
## Racial disparities in Los Angeles traffic stops

This project will reproduce parts of the [Stanford Open Policing Project](https://openpolicing.stanford.edu), which found racial disparities in traffic stops in 20 U.S. states between 2011 and 2015.  The Stanford working paper published in 2017 was a large-scale analysis across the U.S.  This project will focus on traffic stops in the city of Los Angeles and explore similarities and differences with the national findings.  The Stanford project was done in R, so another focus of this project will be on documenting the methodology using Python.   

Here are the main components to the Stanford project.
1.  **Data collection:**  The team gathered the raw data through public records requests and a lot of hard work (understatement of the year).  For this project I will use the Stanford raw data.  A future phase of this project may include comparing this data to the traffic stop datasets available through the city of Los Angeles open data portal.  The full raw dataset includes over 60 million records.

2.  **Data cleaning:**  "\[The Stanford team's\] complete data cleaning pipeline is extensive, requiring subjective decisions and thousands of lines of code."  I will not try to reproduce the entire pipeline, but rather focus on key steps.  Examples: <br>

* Imputing Hispanic ethnicity after performing string edits to names and matching the names from a known Hispanic surname dataset. <br>
* A "spurious density of stops...occurring at precisely midnight" led to the team's assumption that this was actually missing information.<br>  
* Duplicate rows of data may indicate that a row is a violation, not a stop (i.e., a driver may be cited for one or more violations per stop).<br> 
* The Stanford team classified only white, black and Hispanic drivers, as there were relatively few stops of people in other race groups.  I may examine if the numbers of Asian drivers in Los Angeles County and the San Francisco Bay Area are significant, although the data probably doesn't include data from law enforcement jurisdictions with the largest concentrations of Asians, e.g., Monterey Park.

3.  **Analysis:**  In addition to basic EDA, here are the phases from the Stanford study that I'll attempt.      
    1.  Stop rates: The Stanford study found that, nationwide, black drivers were stopped more often than white drivers relative to their share of the driving-age population, but that Hispanic drivers were stopped less often than whites.  This finding came after adjustments for age, gender, location and year.  I will try to reproduce these adjustments, probably using "lower-level" statistical methodologies than the Stanford team.  
    2.  Post-stop outcomes:  After being stopped, a driver can be given a warning, ticketed, searched and/or arrested.
    3.  Searches:  The outcome for a search is whether contraband was found.
