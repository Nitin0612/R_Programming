# R_Programming

**Practice Question For Company_Profit :**

**Question 1:  Which company has the highest profit?**

```R
company_profit <- read.csv("company_profit.csv")
highest_profit_company<- max(company_profit$Profit)

#Print the highest profit value
print(highest_profit_company)

#Find and print the name of the company with the highest profit
highest_profit_company_name <- company_profit$Company.Name[company_profit$Profit == highest_profit_company]
print(highest_profit_company_name)
```
**Output:**

```
[1] 4975093
[1] "Company 20"
```
**Question 2: Which company has the lowest profit?**
```R
company_profit <- read.csv("company_profit.csv")
lowest_profit_company<- min(company_profit$Profit)

# Print the lowest profit value
print(lowest_profit_company)

# Find and print the name of the company with the lowest profit
lowest_profit_company_name <- company_profit$Company.Name[company_profit$Profit == lowest_profit_company]
print(lowest_profit_company_name)
```

**Output:**
```
[1] -795996
[1] "Company 92"
```
**Question 3:What is the average profit across all companies?**
```R
company_profit <- read.csv("company_profit.csv")
average_profit_company<- mean(company_profit$Profit)

# Print the average profit value
print(average_profit_company)
```
**Output:**
```
[1] 2095144
```

**Question 4:What is the distribution of profits across all companies? (Histogram)**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Create a histogram of profits
hist(company_profit$Profit, 
     main = "Histogram of Profits", 
     xlab = "Profit", 
     ylab = "Frequency", 
     col = "blue", 
     border = "black", 
     breaks = 20)
```
**Output:**

![image](https://github.com/user-attachments/assets/63523d26-2342-4453-9583-2dce96f0e311)

