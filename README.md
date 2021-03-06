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
This would visualize the user's ratings for a restaurant. A user that likes every food type is visualized as follows:
<p align="center">
  <img src="https://github.com/VictoryJin/Maps/blob/master/img/likes_everything.png" alt="Labeled Ratings"/>  
</p>

The yellow region represents 5 stars, and thus shows the region where the user potentially might like, whereas the blue region represents 1 star. The above image shows the the user that "likes_everything" with K = 5.  
Using these data, we can predict a user's ratings for unrated restaurants.  
To do so, run:  
```
python3 recommend.py -u #username -k #int -p
```
which would produce the below image:
<p align="center">
  <img src="https://github.com/VictoryJin/Maps/blob/master/img/likes_everything_pred.png" alt="Prediction"/>  
</p>  

This shows a restaurant prediction for all restaurants near Berkeley in the Yelp academic dataset.

#### Inputting Data
Copy a file from the [/users](https://github.com/VictoryJin/Maps/tree/master/users) folder, and copy a user.  Rename the user and input restaurants in the following format, with the ratings:  
```
make_review('Jasmine Thai', 4.0) #restaurant, rating
make_review('Top Dog 2', 4.5)
...
```
To get the list of restaurants in the Yelp academic dataset, 
```
python3 recommend.py -r
```

#### Contributions

Tests and codes implementing graphics were provided by UC Berkeley, with visualization package by D3.
