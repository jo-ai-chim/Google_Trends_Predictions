<p align="center">
  <a href="https://github.com/jo-ai-chim/Google_Trends_Predictions">
    <img src="./Pics/photo-1570303345338-e1f0eddf4946.jpg" alt="Predicition logo" width="408" height="272">
  </a>
</p>

<h2 align="center">Are predicitions based on Google Trends data better than gambling?</h2>

<p align="center">
  A brief introductory analysis if Google Trends data can be used to have a look in the future - by trying to predict the share price of the german stock index DAX. 
  <br>
  <a href="https://github.com/jo-ai-chim/Project_Google_Trends_Prediction"><strong>Explore the code »</strong></a>
</p>

**Spoiler alert: Yes they are!**

After I discovered Google Trends I directly wondered myself if the data can be used for more than just some party games. So I set up a small project trying to get an answer to this question. After reading this article I hope you agree that there is a big potential in using the google trends data and that you can't stop of thinking about potential use cases.

For my analysis I picked the share price of the german stock index DAX. Since "money makes the world go round" I thought this might nbe a good pick. Moreover the data can be easily accessed via [yahoo-finance](https://de.finance.yahoo.com/).

Before making a prediction I tried to answer the question

**How far in the future it might even be possible to make predictions for?**

To get an answer I checked the correlation between the search terms I picked for making the prediction and the share price of the DAX in the next 30 days.

<p align="center">
  <a href="https://github.com/jo-ai-chim/Google_Trends_Predictions">
    <img src="./Pics/correlation.png" alt="Correlation analysis I" width="408" height="272">
  </a>
</p>

As you can see from the graph above the result was quite stunning. (At least for my example) the correlation doesn't seem to depend on how far you want to look into the future. So to continue I chose trying to predict the share price in 30 days.

<p align="center">
  <a href="https://github.com/jo-ai-chim/Google_Trends_Predictions">
    <img src="./Pics/correlation_final.png" alt="Correlation analysis II" width="816" height="544">
  </a>
</p>

Since the correlation for some search terms I piced were quite big (as you can see from the picture above) I was quite optimistic when I tried to answer the second question

**Is it possible to make a good prediction?**

For simplicity and since it is only about the question if it is possible to make a prediciton that makes sense let's use a simple linear regression model. After training it I checked the coefficient of determination (R squared). Based on my initial search terms I got an R squared of 0.5611 when testing the trained model. 

Mh, this is not too good but still good enough to keep going. So since it is about google trends data the first question to answer when trying to improve the model is 

**Does adding more search terms improve the prediction?**

So I added 23 more search terms to my initial set of 17 search terms. And started all over again with training the model. The result was quite satisfying. I got an R squared of 0.8173 when testing the model (I also checked the R squared of the training set by the way to be sure I am not dealing with an case of overfitting).

Having all the possible ways in mind to improve the model and the prediction (like adding other data sources to the input data to train the model, optimizing the selection of the used search terms, analyse different kind of models, etc.) I am convinced:

**Based on google trends data good models can be set up to have a look in the future.**
