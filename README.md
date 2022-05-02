# Sentimental-Analysis--Boston-AirBNB-Reviews
**Sentimental Analysis done on the reviews of various properties listed on AirBNB in Boston.**

Data collected from Data World. 

https://data.world/taise/boston-reviews-2019/workspace/file?filename=reviews%202020.csv

First the data was imported into R.

This is our original Dataset.

![DataSet](https://user-images.githubusercontent.com/97380339/165306218-ed029427-0c4c-4d26-b9de-cc088931cc4d.png)

There are 4993 unique properties listed in the dataset. 
We arranged them by the number of reviews for each property and chose to do the analysis on the one which had the most number of reviews.

![Unique Listngs](https://user-images.githubusercontent.com/97380339/165309058-57cba2c3-4036-4280-a862-36c94139b120.png)

So, the property with listing id = 66288 is the one with maximum reviews (622), and so we try to analyse the sentiment of people about this property.

![Corpus 1](https://user-images.githubusercontent.com/97380339/165315314-606583ea-01cf-4066-9a63-a531d86b744d.png)

We will extract the comments section because we need only the text (Reviews).
First we clean our data and create a final corpus where the data does not have uppercase letters, punctuations, stopwords, and white spaces.

Our final corpus looks like this.

![Screenshot (73)](https://user-images.githubusercontent.com/97380339/165315912-34b654fd-814f-4302-a120-57110fd7211e.png)

Now we create a term document matrix.

![Screenshot (75)](https://user-images.githubusercontent.com/97380339/165316524-1fa05621-7173-47e4-961d-c310637873a9.png)

And then we plot this matrix to see a general view of our data.

![Screenshot (79)](https://user-images.githubusercontent.com/97380339/165318034-38f89ac4-a4f6-4408-9e8f-9a069cc1c0a2.png)

So we can see some positive words in bold, and so it seems like the sentiment might be positive.

So we see that some words like "Sean", "Apartment", "Place" and "Night" appear many times, but they don't add any sentiment.
So we'll remove these words from our term document matrix and create a new one.

Next we'll create a Word Cloud of our final Term Document Matrix, just to get a visual idea of the sentiments in our data.

![WordCloud](https://user-images.githubusercontent.com/97380339/165319286-e031409a-02ba-48ad-b47c-bebc539a1f9a.png)

Now we'll create a NRC Emotion Lexicon and find out the sentiment score.

![Sentiment Score](https://user-images.githubusercontent.com/97380339/165321870-c66149a8-6f45-4faa-9d63-fda51403e260.png)

**So, the first 10 comments have positive score, which means the sentiment is positive in these. Let's see the overall sentiment of all reviews.**

![Sentiment Score](https://user-images.githubusercontent.com/97380339/165322391-ac47c02f-a64c-4d1e-bb80-c7886985f7fa.png)

As we can see, the score is positive and a large value at that, which means that the overall sentiment of all the reviews for this property is largely positive.
We'll plot it and see the result of our analysis.

![Sentiment Plot](https://user-images.githubusercontent.com/97380339/165323030-d2965308-c68a-4406-8e39-df26d3acbcd5.png)


So we can see that the scores for most of the negative sentiments like anger, disgust, and sadness are pretty low.
Whereas most of the positive sentiments like joy and trust have high scores.

So we found out that the sentiment for the property with listing_id = '66288' is Largely Positive.

Now we'll do the same analysis for 10 more properties, (the top 10 with most number of reviews) and visualize our results in Tableau.

[Tableau Visulization of properties with most reviews (Top 10)](https://public.tableau.com/app/profile/daniya.qureshi/viz/SentimentAnalysis-BostonAirBNBReviews/AirBNBLisitings)

![Tableau Viz](https://user-images.githubusercontent.com/97380339/165324319-bd43f597-8140-43ab-b237-e62067669c2c.png)


