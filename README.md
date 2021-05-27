# IMDb Movies Project
 This project is concerned with working on a movie database that came from IMDb which contains information about 10,000 movies from 1960 to 2015.
 
 **This dataset contains the following columns:**
> 
>- id : Movie id                     
>- imdb_id  : Movie Id on IMDb              
>- popularity : Movie popularity (The operational definition for this column and how it was calculated was not mentioned which make this a defect in this database)           
>- budget     : Movie budget             
>- revenue    : Movie revenues            
>- original_title         : Movie Title
>- cast               : Some cast members
>- homepage              : The homepage for the website of each movie
>- director               : Director(s) Name
>- tagline                : Movie Slogan
>- keywords               : searching Keywords(added by the users)
>- overview               : Brief overview of the movie
>- runtime                : Total runtime of a movie in minutes
>- genres                 : Movie different genres (added by users)
>- production_companies   : Name of production companies that produced this movie
>- release_date           : Movie release date
>- vote_count             : Number of votes
>- vote_average          : Average voting score
>- release_year          : Movie release year
>- budget_adj            : Movie budget in terms of 2010 inflammation
>- revenue_adj     : Movie revenues in terms of 2010 inflammation


**In this dataset we defined 3 main dependent variables which are:** 

>- 1- **The financial state of the movie** either with gaining profits or with loss. 
>> In order to deal with the financial state of movies I made 2 new data frames for movies with profits and the other for those who have lost money represented in a new column in each named profit and loss respectively.
>> I also used budjet_adj and revenue_adj column to calculate them in terms of 2010 inflammation to provide some consistency in the analysis process.

>- 2- **The popularity of each movie** using he average voting score for each movie.
>> The results in this section may encounter some bias problems for movies with low voting count, so I decided to include only movies with vote count more than 30
>> I depended on this score to guide my analysis for popularity, so for some analytical processes I decided to be more firm and accept vote average scores with vote count more than 100 to get more representative results and reduce bias as it is more common for popular movies to be more popular among people, and hence have more voting count.

>- 3- **Popularity score**
>> As I mentioned before, The operational definition for this column and how it was calculated was not mentioned which make this a defect in this database, so I decided not to depend on this column to guide my results, but only used it for the sake of clarification as it will be more clearer during the analysis process.


**In this dataset we defined 4 main independent variables which are:**

>- 1- **The production companies of each movie**
>>- When dealing with this column it should be clear that we did not have information about the net profit of each company, so we used the profits of movies that this company was a part of to gain some insights.
>>- We also did not have information about the mother company for each company and did not aggregate them together, we only dealt with each company alone.
>>- Some of the movies are produced with more than one company not only one, so we should be careful before making any judgments.

>- 2- **The director of the movie**
>>- We should be aware here that some movies have more then one director
>>- In order to get more precise results I compared only the top 100 directors that participated in movies

>- 3- **Movie Genres**
>>- This section was entered by Users, so the results may not be very precise
>>- Also in most cases all the movies fall into more than one category, so we will discuss this parts as genres involved in movies that got the highest popularity scores, and the biggest profits.

>- 4- **Movie cast** 
>>- In this column we have the names of 4 main actors for each movie 
>>- The order of mentioning them was according to the sequence of appearing in the movie not the size of their roles
>>- In This section also In order to get more precise results I compared only the top 100 actors that participated in movies


**In terms of the previously mentioned variables, we started our journey to have some insights and answer some question that we have as :**

-  `1-What are the top 5 movies That gained most profits, and How popular they were?` 


- `2-What are the top 5 movies associated with biggest loss in money, and How popular they were?`

- `3-What are the top 5 popular movies, and How their profits were ?` 

- `4-Who are the top 5 directors associated with movies That were most popular?`

- `5-What are the top 5 production companies that their movies gained the biggest overall profits?`

- `6-What are the top 10 Genres associated with movies That gained most profits?`

- `7-What are the top 10 Genres associated with movies That were most popular?`

- `8-Who are The top 5 Actors associated with movies That gained most profits, and How popular they were?`

- `9-Who are The top 5 Actors associated with movies That was most popular, and How their profits were?`
