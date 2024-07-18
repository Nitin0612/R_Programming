# R_Programming

**Practice Question For Company_Profit :**

**Question 1** : Which company has the highest profit?

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
