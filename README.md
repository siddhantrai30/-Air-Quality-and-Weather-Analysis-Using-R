# Load the airquality dataset
data(airquality)

# Remove rows with missing values
airquality <- na.omit(airquality)

# 1. Histogram of Temperature Levels
hist(airquality$Temp, 
     main="Histogram of Temperature Levels", 
     xlab="Temperature (°F)", col="lightcoral", border="black")

# 2. Histogram of Ozone for the Month of May
hist(airquality$Ozone[airquality$Month == 5], 
     main="Histogram of Ozone Levels in May", 
     xlab="Ozone (ppb)", col="lightblue", border="black")

# 3. Boxplot of Temperature by Month
boxplot(Temp ~ Month, data=airquality, 
        main="Temperature Levels by Month", 
        xlab="Month", ylab="Temperature (°F)", col="lightyellow")

# 4. Boxplot of Ozone by Month
boxplot(Ozone ~ Month, data=airquality, 
        main="Ozone Levels by Month", 
        xlab="Month", ylab="Ozone (ppb)", col=c("lightgreen","lightblue","lightcoral","lightyellow"))

# 5. Boxplot of Wind Speed by Month
boxplot(Wind ~ Month, data=airquality, 
        main="Wind Speed by Month", 
        xlab="Month", ylab="Wind Speed (mph)", col="lightblue")
