# 01 Overview Of Recommender Systems

## Application of Recommender Systems
Recommender systems are generally applied to recommend products, contents, music, and people. 


## Gathering Interest Data
Learning about users' interest is one crtical step in builiding a good recommender system.  
There are mainly two ways to figure out a user's indivdual tastes and interests:
- explicit
  - rating（potential sparse data + culture difference）
- implicit
  - click data (susceptible to fraud, bots pollution)
  - purchase
  - consume (time spent)
  
 Building a good recommender system requires high quality and quantity of data. 


## Top-N Recommenders
"Top-N" recommender system produces a finite list of the best things to present to a given person.  

![Anatomy of top-N recommender](https://github.com/RuiyeNi/BookNotes/blob/master/BuilidingRecommenderSystems/Files/01_top-N_recommender.png)  

Data store representing the individual interests of each user usually is a big, distributed "NoSQL" data store like Cassandra or MangoDB or memcache and something, because it has to vend lots of data but with very simple queries.   

**(1) Generate recommendation candidates**  
- Based on similarities between the item and the candidiates

**(2) Candidate ranking**  
- Might have access to more information such as average review score
- Boost results for highly-rate or popular items

**(3) Filtering**  
- Eliminate the one already rated
- Use a stop-list to remove items that are potentially offensive   
- Remove items that are below some minimum quality score  
  
  
 ![item-based](https://github.com/RuiyeNi/BookNotes/blob/master/BuilidingRecommenderSystems/Files/01_item-based.png)  
   
 Item-based collaborative filtering is not compicated from an architecture standpoint; the hard part is building up that database of item similarities. 
