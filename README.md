### Gold-Price-Prediction-Using-Sckit-Learn
 - To predict gold prices using a Linear Regression model in scikit-learn, the key parameters required include past gold prices, economic indicators such as USD 
   exchange rates, inflation rates, interest rates, stock market data, and other relevant factors.
 - The goal of the model is to predict the gold price using linear regression, with the primary parameter being the fluctuating USD-INR exchange rate, which serves 
   as a key factor influencing gold prices.
 - To obtain the gold prices for the year 2024 (from 01/01/2024 to 31/12/2024), I referred to the website exchange-rates.org for insights.
 - Using web scraping techniques (BeautifulSoup and Requests),parsed the HTML data to extract the gold price in ounces and then converted it to 22-carat grams for 
   the entire year.

   ![image](https://github.com/user-attachments/assets/359d1fee-e9e1-4cf7-93ce-d2a199979899)

 - Further cleaned the dataframe by:
   -  Formatting the date column
   -  converting the price from ounces to grams
   -  changing the datatype of the date column from object to datetime.
 -  This process resulted in a final dataframe with two columns: Formatted_Date and 22_Carat_GoldPrice.

   ![image](https://github.com/user-attachments/assets/01b0a205-2d28-44da-892b-85dee57eed6c)
 
 - Used the Yahoo Finance API to retrieve the USD-INR closing rates for the year (01/01/2024 to 31/12/2024), cleaned the dataframe, and ultimately obtained a final 
   dataframe with the columns 'Date' and 'USD_INR'.

   ![image](https://github.com/user-attachments/assets/4f75a553-5c2b-4c33-9c37-9093ca27b661)

- Merged the 2 Dataframes using the Date column with Pandas, resulting in a final dataframe containing the columns 'Date', 'Gold_Rate', and 'USD_INR'.

   ![image](https://github.com/user-attachments/assets/0ebd07d1-6106-4a4a-92cd-8f630525426f)
 
 - Created the dependent and independent variables.
 - In my case as we are predicting the Gold Rate hence its DV and USD-INR is IV.

   ![image](https://github.com/user-attachments/assets/0851580b-b375-4053-9403-52158d4d68b2)

 - Using Sklearn.Modelselection split the data into training and testing sets (typically 80% for training, 20% for testing) using train_test_split() function

   ![image](https://github.com/user-attachments/assets/f0d42f8f-80e3-426b-8a8c-4b74f10dcf4b)

 -  Using Linear Regression from Sklearn to build a predictive model
   
   ![image](https://github.com/user-attachments/assets/6fc19b21-f2c7-48ce-8294-0bd6985ce9a8)

 - Once the model is trained, use it to predict gold prices on the data set
 - Using Gradio created the user interface within the Jupyter notebook, allowing the prediction of gold rates based on the USD/INR exchange rate.

   ![image](https://github.com/user-attachments/assets/6a64c859-6846-40e3-a349-c9a136d16013)
