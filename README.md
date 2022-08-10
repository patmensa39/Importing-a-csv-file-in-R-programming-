# Importing-a-csv-file-in-R-programming-

# Importing a csv file 

library(tidyverse)

inspections <- read_csv("inspections.csv")
inspections


### Since the same data can also be found on the internet, we can also import it 
inspections <- read_csv('http://594442.youcanlearnit.net/inspections.csv')

### looking at the content of the data by using the glimpse command
glimpse(inspections)

### Using your own names for the columns 

names <- c('ID', 'DBName', 'AKName', 'License', 'FacilityType', 'Address', 
           'City', 'State', 'ZipCode', 'InspectionDate', 'InspectionType', 
           'Results', 'Violations', 'Latitute', 'Longitude', 'Location') 

### Suppying this to the new inspection data 
inspections <- read_csv('http://594442.youcanlearnit.net/inspections.csv', 
                        col_names = names)

glimpse(inspections) 
### you can see that all the variable names can be seen in the first line
### so we use the skip command to remove the first column or variable
inspections <- read_csv('http://594442.youcanlearnit.net/inspections.csv', 
                        col_names = names, skip = 1)

glimpse(inspections)

