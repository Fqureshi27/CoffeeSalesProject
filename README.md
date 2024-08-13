# Coffee Sales Analysis

## Project Overview
This project analyzes the sales data of a coffee shop to uncover trends and insights that can help improve business decisions. As well as create a dashboard within Excel that utilizes pivot tables and other functions to showcase data to shareholders and provide a deeper understanding as to how the business is doing.

## Objectives
- Clean and Organize Data
  
- Identify overall sales trends.
  
- Understand peak sales times.
  
- Evaluate the performance of different products.
  
- Create dashboard to showcase results of analysis

  ## Data Cleaning and Preperation
  In the inital data preperation phase, I prepared the following tasks:
  
  1. Data loading and inspection
     
  2. Removed any duplicates to avoid misrepresented data
   
  3. Handled any missing values
   
  4. Ensured all columns have appropriate data types.
  
  5. Formatting

  ## Exploratory Data Analysis
  -Utilize Excel functions to find information about customer
  
  -Create Sales Chart of Customer purchases.
  
  -Which products are top sellers?

  ## Data Analysis Techniques:
-XLOOKUP: Used to match customer data across different tables:

    =XLOOKUP(C2,customers!$A$1:$A$1001,customers!$B$1:$B$1001,,0)
  
-Conditional Lookup with XLOOKUP: Applied to retrieve specific customer details based on conditions:

    =IF(XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0)=0,"",XLOOKUP(C2,customers!$A$1:$A$1001,customers!$C$1:$C$1001,,0))
  
-INDEX-MATCH: Employed to extract product information from a list:

    =INDEX(products!$A$1:$G$49,MATCH(orders!$D3,products!$A$2:$A$49,0),MATCH(orders!K$1,products!$A$1:$G$1,0))
  
-Nested IF Statements: Used to categorize coffee types based on product codes:

    =IF(I2="Rob","Robusta",IF(I2="Exc","Excelsa",IF(I2="Ara","Arabica",IF(I2="Lib","Liberica",""))))
  
  
