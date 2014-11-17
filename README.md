# Challenge Week 12 Submission Template

Daniel Nolan

Score: 95/100

# Reddit Data Challenges

## Challenge 1

![Challenge 1](http://i.imgur.com/bso7fBY.png)

## Challenge 2

Running a command with the key set as "mongodb" does not produce any results. Also, there are many subreddits to any searchable reddit topic. 
 ![Challenge 2](http://i.imgur.com/hTm8QbZ.png)
 
## Challenge 3

From this dataset, I could personally track most used profanity words and topics relative to it. With that information, I could track how many actual comments contained profanity as a percentage of the whole Reddit database given. Or, just for fun, find the trends in Reddit at this time. The subreddits are the main place to track these trending topics when organized from most viewed to least.

What do you think this dataset would tell you about the Reddit Community as a whole?

## Challenge 4

As a whole, it would tell me what the most popular topics are among millions of internet users on Reddit. Also, what commonly used words make up main Reddit comments. The words in the picture below were pretty prevalent in the Reddit data which was pretty interesting.
![Challenge 4](http://i.imgur.com/f34io6A.png)

## Challenge 5

Couldn't get this file to work at all. 


## Challenge 6

We are only considering those comments with ten or more upvotes and not identifying those comments that have a large amount of downvotes. Also, some comments may be found offensive on one subreddit from a user but very popular on another. This could change how frequent a said user shows up if they have to gain at least 10 upvotes.  

## Challenge 7

Since you are not including posts with less than 10 upvotes then yes, the number of frequently commenting users in a certain subreddit would vary. Many people access specific subreddits and the mood of upvoting/downvoting varies with what is happening the day. 

## Challenge 8

It only incorporates popular votes with over 10 upvotes and not negative comments/posts.

## Challenge 9

We are only viewing the top 50 subreddits when there are thousands of subreddits that we could have looked at instead.
Also, spammers are very noticeable and the sad souls that love to downvote everyone for no reason.
## Challenge 10

You would have to effectively create a code that can identify top comments that are related to that subreddit first and foremost (to remove spam comments). Then, this code could track downvote patterns and identify downvotes that were input from trolls through a type of Downvote per Minute pattern. Then, the base content of a post/comment could be found legitimate through keywords that mainly pertain to that subreddit ( like the word count example above). 

# Yelp and Weather 

## Challenge 1

![Photo](http://i.imgur.com/ZLatVpp.png)

The total hpcp value came out to be 62.

## Challenge 2
![]()
db.normal.aggregate([{$match:{"DATE":{$regex: /^20100425/}, "STATION_NAME":{$regex: /^LAS VEGAS/}}},{$group: { _id: "$STATION_NAME",avgAmount: {$avg: "$HLY-WND-AVGSPD"}}}])
[Answer]

## Challenge 3
![Challenge3](http://i.imgur.com/EUAdiu2.png)
var query = db.business.find({"city":"Madison","state":"WI"}),array = [], num = db.business.count({"city": "Madison","state":"WI"});

for (var i = 0; i < num; i++) array.push(query[i]["business_id"]);
[1630]
db.reviews.count({"business_id":{$in : array}})
[31305]

## Challenge 4
![Challenge4](http://i.imgur.com/GuMTH5I.png)
var query = db.business.find({"city":"LasVegas","state":"WI"}),array = [], num = db.business.count({"city": "Las Vegas","state":"NV"});

for (var i = 0; i < num; i++) array.push(query[i]["business_id"]);
[12021]
db.reviews.count({"business_id":{$in : array}})
[522104]

## Challenge 5
![Challenge5](http://i.imgur.com/CCilNDB.png)
var query = db.business.find({"city":"Phoenix","state":"AZ"}),array = [], num = db.business.count({"city": "Phoenix","state":"AZ"});

for (var i = 0; i < num; i++) array.push(query[i]["business_id"]);
[7499]
db.reviews.count({"business_id":{$in : array}})
[185907]
