# Exploratory Data Analysis
## Peer-graded Assignment: Course Project 1
### Zana Pekmez; 12.10.2018

###PROJECT HIGH LEVEL DESCRIPTION:
* Dataset was first downloaded from the provided link and working directory set to a desktop folder where .txt date file was saved to:
setwd("~/Desktop/Coursera DS/Exploratory data analysis")

* Dataset has been loaded into R, converted to Date class and appropriatley subsetted. 
read.csv("household_power_consumption.txt",header=TRUE, sep=";", stringsAsFactors=FALSE, dec=".")
data <- read.table("household_power_consumption.txt", header = T, 
+                    sep = ";", na.strings = "?")
data$Date <- as.Date(data$Date, format = "%d/%m/%Y")
data <- subset(data, subset = (Date >= "2007-02-01" & Date <= "2007-02-02"))

* Dates and times have been converted:
data$datetime <- strptime(paste(data$Date, data$Time), "%Y-%m-%d %H:%M:%S")

### NOTE: R code script for each Plot could be find in this REPO as separate R.file corresponding the the name of the plot itself. 
    Thank you!
