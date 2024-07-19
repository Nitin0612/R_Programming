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
