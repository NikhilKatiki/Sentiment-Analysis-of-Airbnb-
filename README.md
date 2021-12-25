# Sentiment-Analysis-of-Airbnb
  1. Introduction
  2. Objective 
  3. Data Dictionary
  4. Data Pre-processing
  5. Feature Engineering 
  6. Sentiment Score Calculation
  8. Results
  9. Tableau Dashboard 
  10. Limitations of Score
# Introduction 
  1.It is not new that pandemic impacted a lot of businesses from closing the business for sometime to complete shutdown of the business <br>
  2.Airbnb is one of those companies who got hit initially and regained over time <br>
  3.To analyze the customer sentiment during this period, Customer sentiment score is calculated and understand the impact of strategies on the customer sentiment score
# Objective 
  1.Airbnb has regained well during covid. It is obvious that the positive customer sentiment decrease at some point and then, suddenly increase <br>
  2.The objective is to understand how sentiment on Airbnb has varied across time and see, what all things have changed in Airbnb during pre-covid and post-covid <br> 
  3.Since the reviews would be very high in number, only 3 cities have been considered for the analysis (which are very different from each other) <br>
# Data Dictionary
  1.Since the sentiment score can only be found from reviews (unstructured data), Reviews data from Airbnb has been used to understand the sentiment of the customer <br>
  2.The dataset contains the following information. Displaying the first 5 rows of the data <br>
  
  3.Only the reviews column is used to find the sentiment of the customer <br>
# Data Preprocessing  
   The reviews data is in string format which needs to be converted to numeric format to find the quantitative sentiment score. Following are the steps <br> 
     1.Tokenization <br>
      &nbsp;&nbsp;&nbsp;&nbsp;    i.The sentences are being tokenized into words<br>
     2.Stemming<br>
       &nbsp;&nbsp;&nbsp;&nbsp;   i.Affixes or Prefixes are removed to reduce the dimensionality and get the words to its base form <br>
     3.Stop words<br>
       &nbsp;&nbsp;&nbsp;&nbsp;   i.Stop words which are frequently used are being removed as these dont contribute to the overall sentiment of the customer <br>
     4.Numeric formats <br>
        &nbsp;&nbsp;&nbsp;&nbsp;  i.Numeric formats have been removed as these are not useful in understanding the review <br>
# Feature Engineering 
   Positive words and Negative words <br>
         &nbsp;&nbsp;&nbsp;&nbsp; i.Finding the number of positive words and negative words for every review <br>
          &nbsp;&nbsp;&nbsp;&nbsp;ii.Storing number of positive words in positive and number of negative words in negative <br>
# Sentiment Score Calculation 
   The score is calculated using the formula: <br>
          Sentiment score = (#Positive)/(#Positive+#Negative) when #Positive>#Negative <br>
                        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;  =-(#Negative)/(#Positive+#Negative) when #Positive>#Negative<br>
# Results 
  1.Sentiment dropped after March 2020, but as the company takes remedial steps, sentiment increased over time <br>
  2.Top positive and negative comments did not change much in pre and post Covid  <br>
  3.Dirty and Crowded are highlighted negative comments post-Covid which can be suggestion to Airbnb hotels which are having low sentiment scores <br>
# Tableau Dashboard 
https://public.tableau.com/app/profile/katiki.nikhil

  
# Limitations of Score 
    1.The list of positive words and negative words is limited to the one which is provided as input 
    2.There are equal weights assigned to each and every word 
    3.The Analysis wont capture the phrases such as "not good". This sentence has neutral score whereas it is to be tagged as negative 
  
