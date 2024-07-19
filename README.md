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
