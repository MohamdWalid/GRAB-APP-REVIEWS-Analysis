## => This data is user reviews of the Grab app.
## => Data
     1) index is the row number.
     2) review_text is a user review.
     3) review_rating is the user's evaluation of the application. (from 1 to 5)
     4) author_id is the user's ID.
     5) author_name is the user's name.
     6) author_app_version is the Version the Review Was Made.
     7) review_datetime_utc is a Review Datetime in UTC.
     8) review_likes is the Number Of Likes Of The Review.

## => Questions
   1) total number of reviews and likes.
   2) total number of Promoter reviews and likes.
   3) total number of Passive reviews and likes.
   4) total number of Detractor reviews and likes.
   5) Do we keep our customers?
   6) Are we seeking to develop the application?

## => Data Preparing
   1) Remove a review text and author_name columns
   2) Replace review_datetime_utc column by Review_Date and Review_Time 
       Columns.
   3) Remove author_id and Review_Time Columns.
   4) there are null values in author_app_version but we can predict version by 
       know the review date and  The version was taken from the review date that 
       was before or after it.
   5) Divide the reviews into three categories:
        a) Promoter => user is satisfied if his review is 4 or 5.
        b) Passive => user is satisfied but not completely satisfied if his review is 3.
        c) Detractor => user is not satisfied if his review is 1 or 2.
       
## => Insights
   1) We have shown several KPIs that measure the actual performance of the 
        application such as Reviews , Likes, Promoter reviews, Likes on promoter 
        reviews, Passive reviews, Likes on passive reviews , Detractor reviews, Likes 
       on Detractor reviews.
      
    2) It seems that we have been losing users since 2019, as the number of 
        reviews and likes has decreased year after year.
        
    3) It seems that we are not improving the application, but rather each version 
       is getting worse than the one before it since 2019, as the percentage of 
       Detractor reviews and likes on them increases year after year, and the 
       percentage of Promoter reviews and likes on them decreases.
