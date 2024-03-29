# Recommender-System  

**EPILOGUE:**    

Imagine a situation where a customer interacts with a very large catalogue of products. This can be movies from Netflix, items from Amazon, Music from Spotify, videos from YouTube or even the apps from play store. What really matters is how the user interacts with the catalogue. One way is if a user knows what he wants is by Search method for the precise item. But for a very large catalogue , users often don’t know what they are looking for exactly. This is where a recommendation system come in. This system recommends to the user certain items that it thinks the user will be interested in based on what they know about the user.  

The aim of this project is to analyse an available dataset from an Ecommerce business and find the hidden patterns &amp; correlating it to the trends. Recommendation engine provides a personalised information to a customer by learning its past purchase history, demographics and other interactions.  

**THEME:**  
  
To produce a generalised, specific and tailored recommendation to a user by observing the pattern in his purchase behaviour using transactional data from an online Ecommerce retailer. To keep on giving more specific recommendations, I have used three different
approaches and tried to explain them in the simplest of manner performing all the computations on a Jupyter notebook and providing snippets wherever necessary.  
  
_a) Affinity based analysis – Based on Affinity Weight, Popularity, Recency_

Sometimes also called Market basket analysis or association rule learning is a data mining technique that can be used in various fields like networking, ecommerce, entertainment, marketing, sales etc . The basic aim of such an algorithm is to help a customer making a better decision while choosing a product. This can be from Amazon which suggests a different product relation with the product from the purchase history (E.g. : Printer --> Paper) or the Android google play store which suggests a related app to the one which you previously downloaded. There are mainly three indices to understand the presence , strength and nature of Affinity mining. These are support, confidence and lift.   
Support : The support of a product A, supp(A) is the proportion of transaction in the database in which the item X appears. It signifies the popularity of an itemset.  
  
**supp(A) = (Number of transactions in which A appears)/(Total number of transactions)**  

Confidence : Confidence signifies the likelihood of product B being purchased when product A is purchased.  
**conf(A --&gt; B) = supp(A U B) / supp( A )**  
_It is more like a conditional probability, P(Y|X), that is probability Y given Probability of X._  
  
Lift : Lift explains the ratio of Confidence &amp; Expected confidence.  
**lift (X --&gt; Y) = supp (X U Y)/( supp(X) supp (Y) )**  
_For two products likely to be bought together, lift needs to be greater than 1_  
  
_b) Similar Customer based analysis – Based on the score/rating given by the customer_  

This is also known as Collaborative Filtering. The basic idea behind building a collaborative filtering is very simple. Suppose we have a customer C1 to whom we need to make recommendations. For this, we need to find a group of other users whose likes and dislikes are similar to the customer C1.  

**Importance** :Collaborative Filtering has a significance of its own that is it does not require to understand the nature of the items and still can suggest complex products. This can be implemented in any kind of recommendation whether books, movies, products, people etc. It doesn’t require any feature selection because to select relevant features form a data like movies or music is quite complicated.  
To compute this, we can use different approaches like Jaccard similarity, Cosine similarity or Pearson similarity.  

_c) Content based analysis – Based on the Review sentiments of the customer_  

This is also known as Content Based Filtering. Here I have used text mining (Sentiment Analysis) to determine the sentiment of the Customer as per the reviews provided for a product and based on this and the average score (rating) given by the customer, I have tried to predict a similar product for a customer.  

**PROBLEMS ASSOCIATED WITH RECOMMENDER SYSTEM**  

_a. Cold Start Problems_  
 New Customers with no purchase history have no recommendations.  
 New Products with no ratings have no recommendations.  
**Solution : Recommending using the popularity matrix – Top N products**  

_b. Sparsity Problem_  
A User – Product Matrix with a dimension of 10M*10M where not every user has rated every other product gives a very sparse matrix.  

_c. Real time Data Manipulation problem requires costly stream processing hardware._
Computation of a 10M products will need a matrix of 10M*10M entries which will take a huge toll out of the memory and time complexity.  
**Solution : This can be avoided by applying Dimensionality Reduction techniques like SVD or PCA.**  

_d. Explore versus exploit_  
Trade-off between recommending very similar products (Know the user likes these) Recommending new products (New products the user may like but we and/or user don’t know it yet)    
**Solution : Active Learning**    

_e. Fraud Recommendation_  
To increase the profitability of the merchants, products with higher sales margin are recommended to the user and that with lower margin is not recommended. Also, in some cases, a seller tends to recommend a different product of his own brand and weights down the ranking of the competitor brand.  
**Solution : Content based filtering tends to avoid this incorrect way of prediction**  

**CONCLUSION**  

For this project there have been a variety of things which have helped me put theory into practical learning which is used in real world scenarios. One such problem is associated with data collection. Most of the times, we obtain the data in an unstructured or a semi
structured format. Exploratory data analysis (EDA) forms a major part to get a feel of the data. Once the data is cleansed, we apply various transformations on it (Feature Engineering) according to our requirements in order to receive the desired result. Now nMachine learning algorithms comes into play which helps us in prediction. Finally, the output is interpreted and evaluated using the statistical methods.  
