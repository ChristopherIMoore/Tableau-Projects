# Tableau Projects
This repository contains Tableau dashboard and Analysis I have competed regarding 2 seperate projects
* Analyzing Audible data
* Analyzing Seattle Airbnb data

These projects can also be found at my Tableau public profile - https://public.tableau.com/app/profile/christopher.moore4696/vizzes

## Audible Project

### Aim of Project
Visualize the Audible data to highlight the spread of language, price and number of releases since 1999.
To discover 
* Spread of audio books across each language
* The number of audio books released each year
* Highest rated authors
* Average price of audio books dependent on language
* If more expensive audio books are more highly rated

### Context
Audible has been around since 1995 however in 1997 they started to release audio books. In 1999 Microsoft invested 11 million USD into the company and since then Amazon bought Audible in 2008. Since then, Audible has grown in popularity and use so this project was made to gain an overview of Audibles data and to demonstrate my ability to use Tableau.

### CSV changes
Before I uploaded this csv to Tableau, I added a new column (GBP price). The reason for this is that the price of these audio books was in Indian Rupees as this data set was formed in India and I wanted to visualise the price of these books in Great British Pounds. To do this I used the current exchange rate of 1 INR to 0.009140 GBP and multiplied the value in the price column with the exchange rate resulting in the price being in GBP. 

### Tableau Editing for creating tables
* Created an ID column for counting the rows

As there was no ID column in this data I created a column where every value is 1. What this enabled me to do is count each row of data as 1 creating an accurate count of Audio Books Released per Language. This would also enable me to create a rolling total where I could also count from. 

* Created AVG stars exclusing 0

Star reviews go from 1 - 5 however there was a large portion of audio books that have not been reviewed meaning when looking for average ranking per price point it would skew the data making the average star review lower than it should be, to fix this I made a calculated feild with this code (FLOAT(AVG( IIF( [Stars] = 0, Null, [Stars] )))) to remove all 0 stars meaning the data will no longer be skewed.

* Grouped Price into price ranges

I grouped the priceing into ranges of £5 up into everything over £30. The reason for this was it enabled me to create the visulisation to see if certain price ranges are more highly rated

### Picture of the Visulisation
![Alt text](Audible-Project/Audible%20Data%20Dashboard.png)
### Analysis
By Far the most common language used is English which makes sense as Audible only started opening up to other markets using other languages.
English also has the most expensive average price however more expensive books are typicly the lowest rated and the highest rated are the ranges of £10 - £14.99 and followed closly by £5 - £9.99.
The most popular authors are Kristen Ashley, Osho & Gertrude Chandler Warner but the 10th most popular is Innovative Language Learning with a sharp decrease of 0.38 from 9th place of Nora Roberts. 
Overall English books dominate the market with the most popular books being priced around £5 - £15. 

Dataset: https://www.kaggle.com/datasets/snehangsude/audible-dataset

## Seattle Airbnb Project
### Aim of Project
Visulise the Airbnb Market in Seattle to help inform new prospecting Airbnb hosts on the market 
* Find the Average price based on Zipcode
* Find the Average price based on bedrooms
* Find the bext time to open the Airbnb
* Find how much compatatition each 

### Context


### CSV changes


### Tableau Editing for creating tables
