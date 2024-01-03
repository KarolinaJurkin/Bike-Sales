# Bike Sales

![image](https://github.com/KarolinaJurkin/Bike-Sales/assets/53952580/30954feb-eec2-4d90-922a-73d65668a85a)



### Tools and resources used

- Data provided by Alex Freberg 
- Excel - data cleaning, analyzing data and creating dashboard
### Data cleaning

My first step was to copy the raw data to 'Calculations' sheet and then remove duplicates. I decided to use 'Remove Duplicates' feature in Excel, because my data is not going to be updated and I don't need it to be dynamic. 26 rows were removed as a result. 

Next I used 'Find and Replace' feature to update the 'Marital status' column: 
- 'M' -> 'Married'
- 'S' -> 'Single'
And 'Gender' column:
- 'F' -> 'Female'
- 'M' -> 'Male'

To make sure I didn't miss any values I applied filters to see what distinct entries are in both columns. Then I went through all columns and looked at the unique values. 

In order to bin age information into meaningful ranges I first inserted a column 'Age bracket'. Then I created lookup values in seperate cells and named them 'LookupAge'. I used VLOOKUP function to populate the newly created column with approximate match.
In order to find ranges that would be informative I tried to split the data into as equal increments as possible. I used the COUNTIFS function to find these ranges. Since I have 1000 records I tried to make each range as close to 200 (1000/5) as possible. 
### Data Analysis

I started with creating a table from my cleaned data. Then on a separate worksheet I inserted a pivot table. 

I decided to look at the number of cars owned versus bike sales. Data confirmed my suspicion that people with less cars would more often purchase a bike. The possible explanation for this could be that bikes are more often used as a commute (not only to work) option for people with less cars. 

When I looked for a correlation between number of children and bike purchases I was surprised to find that large families tend to buy bikes less often. 

Next step was to compare commute distance with bike purchases. The values here varied and it's hard to come up with unambiguous conclusion other than that 10+ Miles of commute distance significantly lowers the chances of someone buying a bike.

Lastly I checked what role age played in bike sales. I used the age brackets I created previously and it shows that the group that buys bikes most often is early middle age people.

I am sure the income level also plays an important factor on bike purchases. Unfortunately this dataset doesn't provide enough information to calculate family income. We would need additional data about the spouse/partner income to calculate it. 

