R Programming Quiz_1

Load data

setwd("C:\R") data1 <- read.csv("quiz_1.CSV", header = TRUE)

In the dataset provided for this Quiz, what are the column names of the dataset?

colnames(data)

Extract the first 2 rows of the data frame and print them to the console. What does the output look like?

data1 <- data1[1:2, ]

data1

How many observations (i.e. rows) are in this data frame?

tail(data)

Extract the last 2 rows of the data frame and print them to the console. What does the output look like?

data1 <- data1[152:153, ]

data1

What is the value of Ozone in the 47th row?

data1&Ozone[47]

How many missing values are in the Ozone column of this data frame?

missingNA <- is.na(data1$Ozone)

as.numeric(missingNA)

sum(missingNA)

What is the mean of the Ozone column in this dataset? Exclude missing values (coded as NA) from this calculation.

Ozone <- na.omit(data1$Ozone)

as.numeric(Ozone)

mean(Ozone)

Extract the subset of rows of the data frame where Ozone values are above 31 and Temp values are above 90. What is the mean of Solar.R in this subset?

	data1.sub0 <- data1[data1$Ozone > 31, , drop = FALSE]

	data1.sub1 <- data1.sub0[data1.sub0$Temp > 90, , drop = FALSE]

	data1.sub2 <- na.omit(data1.sub1)

	mean(data1.sub2$Solar.R)

What is the mean of "Temp" when "Month" is equal to 6?

data1.June <- data1[data1$Month == 6, , drop = FALSE]

mean(data1.June$Temp)

What was the maximum ozone value in the month of May (i.e. Month is equal to 5)?

data1.May <- data1[data1$Month == 5, , drop = FALSE]

max(data1.May0$Ozone)