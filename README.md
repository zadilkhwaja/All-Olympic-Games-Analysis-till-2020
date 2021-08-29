# Summer Olympic Games Analysis

## __Business Problem__

The challenge for this data analyst project is outlined below. This has been used continuously to ensure that the right data has been selected, transformed and used in the data visualization which is meant to be passed on to the business users.

“As a data analyst working at a news company you are asked to visualize data that will help readers understand how countries have performed historically in the summer Olympic Games.

You also know that there is an interest in details about the competitors, so if you find anything interesting then don’t hesitate to bring that in also.

The main task is still to show historical performance for different countries, with the possibility to select your own country.”

## __Data Collection & Table Structures__

The necessary data was first put into a SQL database and afterwards transformed using the transformations that you can see below.

### __Olympic Games View__

![hi](https://user-images.githubusercontent.com/46615169/131238204-022f0875-0d04-4f66-b3f1-530f0d23b3e2.PNG)
  
## __Data Model__

As this is a view where dimensions and facts have been combined, the data model that is created in Power BI is one table. The query from previous step was loaded in directly.

![olympicgamesanalysis3](https://user-images.githubusercontent.com/46615169/131238241-c08278df-fba4-40c7-afba-cf9d37bcf258.png)

## __Calculations__

The following calculations were created in the Power BI reports using DAX (Data Analysis Expressions). To lessen the extent of coding, the re-use of measures (measure branching) was emphasized:

Number of Competitors:

#### # of Competitors = DISTINCTCOUNT( ‘Olympic Data'[ID] )

#### # of Medals = COUNTROWS( ‘Olympic Data’ )

#### # Of Medals (Registered) = CALCULATE( [# of Medals], FILTER( ‘Olympic Data’, ‘Olympic Data'[Medal] = “Bronze” || ‘Olympic Data’ [Medal] = “Gold” || ‘Olympic Data'[Medal] = “Silver” ))

## __Olympic Games Analysis__

The finished dashboard consist of visualizations and filters that gives an easy option for the end users to navigate the summer games through history. Some possibilities are to filter by period using year, nation code to focus on one country or look into either a competitor or specific sports over time.
