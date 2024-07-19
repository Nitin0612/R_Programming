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


**Question 5:What is the average profit per employee for each company?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Calculate the average profit per employee for each company
company_profit$Profit_per_Employee <- company_profit$Profit / company_profit$Number.of.Employees

# Select and print the company name and profit per employee
average_profit_per_employee <- company_profit[, c("Company.Name", "Profit_per_Employee")]

#To print all companies
print(average_profit_per_employee)

#To see top companys
head(average_profit_per_employee)
```
**Output:**
```
A data.frame: 6 × 2
Company.Name	Profit_per_Employee
<chr>	<dbl>
1	Company 1	20594.6159
2	Company 2	4942.7783
3	Company 3	46098.4051
4	Company 4	-909.4085
5	Company 5	14144.6460
6	Company 6	585.9745
```
**Question 6:Which are the top 5 companies by revenue?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Find the top 5 companies by revenue
top_5_revenue <- head(company_profit[order(-company_profit$Revenue), ], 5)

# Select and print the company name and revenue
top_5_revenue <- top_5_revenue[, c("Company.Name", "Revenue")]
print("Top 5 Companies by Revenue:")
print(top_5_revenue)
```
**Output:**
```
[1] "Top 5 Companies by Revenue:"
   Company.Name Revenue
66   Company 66 9891087
26   Company 26 9829778
65   Company 65 9767124
39   Company 39 9708898
12   Company 12 9699352
```

**Question 7:Which are the top 5 companies by profit?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Find the top 5 companies by profit
top_5_profit <- head(company_profit[order(-company_profit$Profit), ], 5)

# Select and print the company name and profit
top_5_profit <- top_5_profit[, c("Company.Name", "Profit")]
print("Top 5 Companies by Profit:")
print(top_5_profit)
```
**Output:**
```
[1] "Top 5 Companies by Profit:"
   Company.Name  Profit
20   Company 20 4975093
12   Company 12 4916471
18   Company 18 4909830
60   Company 60 4843891
5     Company 5 4795035
```
**Question 8:What is the distribution of revenues across companies? (Boxplot)**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Create a boxplot of revenues
boxplot(company_profit$Revenue,
        main = "Boxplot of Revenues",
        ylab = "Revenue",
        col = "blue",
        border = "black")
```
**Output:**

![image](https://github.com/user-attachments/assets/c25cacde-6d98-42f0-9ae2-16ae685dc73c)

**Question 8:Are there any companies that have a negative profit? How many are there?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Find companies with negative profit
negative_profit_companies <- company_profit[company_profit$Profit < 0, ]

# Count the number of companies with negative profit
num_negative_profit_companies <- nrow(negative_profit_companies)

# Print the result
print("Number of companies with negative profit:")
print(num_negative_profit_companies)
```
**Output:**
```
[1] "Number of companies with negative profit:"
[1] 15
```
**Question 9:What is the total expenses incurred by all companies combined?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Calculate the total expenses
total_expenses <- sum(company_profit$Expenses)

# Print the result
print("Total expenses incurred by all companies combined:")
print(total_expenses)
```
**Output:**
```
[1] "Total expenses incurred by all companies combined:"
[1] 477773338
```
**Question 10:What is the total revenue generated by all companies combined?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Calculate the total revenue
total_revenue <- sum(company_profit$Revenue)

# Print the result
print("Total revenue generated by all companies combined:")
print(total_revenue)
```
**Output:**
```
[1] "Total revenue generated by all companies combined:"
[1] 537550858
```
**Question 11:What is the average expense per company?**
```R
# Load the CSV file
company_profit <- read.csv("company_profit.csv")

# Calculate the average expense per company
average_expense <- mean(company_profit$Expenses)

# Print the result
print("Average expense per company:")
print(average_expense)
```
**Output:**
```
[1] "Average expense per company:"
[1] 4777733
```
