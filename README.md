# Recommender-System  

**EPILOGUE:**    

Imagine a situation where a customer interacts with a very large catalogue of products. This can be movies from Netflix, items from Amazon, Music from Spotify, videos from YouTube or even the apps from play store. What really matters is how the user interacts with the catalogue. One way is if a user knows what he wants is by Search method for the precise item. But for a very large catalogue , users often don’t know what they are looking for exactly. This is where a recommendation system come in. This system recommends to the user certain items that it thinks the user will be interested in based on what they know about the user.  

The aim of this project is to analyse an available dataset from an Ecommerce business and find the hidden patterns &amp; correlating it to the trends. Recommendation engine provides a personalised information to a customer by learning its past purchase history, demographics and other interactions.  

**THEME:**  
  
To produce a generalised, specific and tailored recommendation to a user by observing the pattern in his purchase behaviour using transactional data from an online Ecommerce retailer. To keep on giving more specific recommendations, I have used three different
approaches and tried to explain them in the simplest of manner performing all the computations on a Jupyter notebook and providing snippets wherever necessary.  
  
_a) Affinity based analysis – Based on Affinity Weight, Popularity, Recency.  _

Sometimes also called Market basket analysis or association rule learning is a data mining technique that can be used in various fields like networking, ecommerce, entertainment, marketing, sales etc . The basic aim of such an algorithm is to help a customer making a better decision while choosing a product. This can be from Amazon which suggests a different product relation with the product from the purchase history (E.g. : Printer --> Paper) or the Android google play store which suggests a related app to the one which you previously downloaded. There are mainly three indices to understand the presence , strength and nature of Affinity mining. These are support, confidence and lift. 
Support : The support of a product A, supp(A) is the proportion of transaction in the database in which the item X appears. It signifies the popularity of an itemset.
**supp(A) = (Number of transactions in which A appears)/(Total number of transactions)**

Confidence : Confidence signifies the likelihood of product B being purchased when product A is purchased.
**conf(A --&gt; B) = supp(A U B) / supp( A )**
_It is more like a conditional probability, P(Y|X), that is probability Y given Probability of X._

Lift : Lift explains the ratio of Confidence &amp; Expected confidence.

**lift (X --&gt; Y) = supp (X U Y)/( supp(X) supp (Y) )**
_For two products likely to be bought together, lift needs to be greater than 1_

_b) Similar Customer based analysis – Based on the score/rating given by the customer.  _  


c) Content based analysis – Based on the Review sentiments of the customer.  
