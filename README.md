# Maps
#### Introduction
Maps using Yelp academic dataset to visualize data using K-means and Voronoi diagrams.    
The current code allows for variable k, the number of clusters.  
For initialization of graphic visualization install the most recent version of [Python3](https://www.python.org/downloads/) and run,
```
python3 recommend.py -u #username -k #int
```
Replace #username with a registered user in the directory [/users](https://github.com/VictoryJin/Maps/tree/master/users).  
Replace #int for a positive number to set k, the number of clusters.  
This would visualize the user's ratings for a restaurant. A user that likes expensive restaurants be visualized as follows:
<p align="center">
  <img src="https://github.com/VictoryJin/Trend_Analyzer/blob/master/Images/US%20Unemployment%20Comparison.png" alt="Unemployment in US vs. Google"/>
  <center>*User = likes_expensive, K = 5*<center/>
</p>

The yellow region represents 5 stars, and thus shows the region where the user potentially might like, whereas the blue region represents 1 star.  
Using these data, we can predict a user's ratings for unrated restaurants.  
To do so, run
```
python3 recommend.py -u #username -k #int -p
```
<p align="center">
  <img src="https://github.com/VictoryJin/Trend_Analyzer/blob/master/Images/US%20Unemployment%20Comparison.png" alt="Unemployment in US vs. Google"/>
  <center>*User = likes_expensive, K = 5*<center/>
</p>
This shows a restaurant prediction for all restaurants near Berkeley in the Yelp academic dataset.

#### Contributions

Tests and codes implementing graphics were provided by UC Berkeley, with visualization package by D3.
