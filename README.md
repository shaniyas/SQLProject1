## Team Name
21479 Group 6


## Team Members

- [Shaniya Scales](https://www.github.com/shaniyas)

- [Saniya Bedi](https://github.com/Saniya-Bedi)

- [Charlie Jones]()

## Project Description
Letterboxd is a social media platform for film lovers, where users can log, rate, review, and discuss movies. The platform includes features like user profiles, movie ratings, reviews, lists, and social interactions. Our SQL program aims to store and organize this data for easy retrieval.

## Data Model
 Our model is based on the structure of Letterboxd, a social media platform for film enthusiasts. The User entity represents individuals who engage with the platform by reviewing, rating, and discussing movies. Each user can have multiple activities recorded, such as logging in, commenting, and subscribing to different membership tiers. This is represented by the one-to-many relationship between the User entity and the Activity and Comments entities.

The core of the model revolves around movies. The Movie entity stores information such as title, genre, country of origin, runtime, and release date. Each movie is directed by a filmmaker, which establishes a one-to-many relationship between the Directors entity and the Movie entity, as a single director can be responsible for multiple films.

Movies also feature actors, which is reflected in the Cast table. Since a movie can have multiple actors, and an actor can appear in multiple movies, we establish a many-to-many relationship between the Movie and Actor entities, which is managed by the Cast associative table. The Cast table records additional details, such as the role type and character name of the actor in the respective film.

Users engage with movies by writing reviews, which is captured in the Reviews table. A one-to-many relationship exists between the User and Reviews entities because a user can submit multiple reviews, but each review belongs to only one user. Similarly, a one-to-many relationship is established between Movie and Reviews, as a movie can have multiple reviews.

More user engagement is represented by the Comments table. Users can comment on movie reviews, which forms a one-to-many relationship between Reviews and Comments, as each review can have multiple comments. Each comment is tied to a specific user, creating another one-to-many relationship between the User and Comments entities.

The platform operates on a subscription-based model, which is reflected in the Subscriptions entity. Users may subscribe to different tiers, such as Free, Pro, or Patron, to unlock various platform features. The BillingHistory table captures payment transactions related to these subscriptions. There is a one-to-many relationship between User and BillingHistory, as a user can have multiple subscription payments over time. Similarly, a one-to-many relationship exists between Subscriptions and BillingHistory, as each subscription type can be linked to multiple transactions.

<img width="917" alt="Screenshot 2025-03-17 at 1 11 45 PM" src="https://github.com/user-attachments/assets/d0457f75-6f2f-4be3-a5cb-4ce9258e04b2" />

## Data Dictionary
[screenshot]

## Queries
[query matrix table] , [explanation/justification of each query], [screenshot of results]


1. Query 1 displays the list of users who made their account before 2024 and have not written any reviews yet. Query 1 allows the managers to see which accounts are inactive. It is expensive to run a platform with many users, so by deleting any inactive accounts, the managers are able to cut down on costs. The deletion of inactive users also improves the security of the platform, as these accounts tend to be more susceptible to hacking.
<img width="1150" alt="TPQ1 updated" src="https://github.com/user-attachments/assets/a19c9dbd-e2d1-4fa9-867a-838ba0b12265" />






2. Query 2 displays the total amount of revenue made from users from countries outside of America, with the results grouped by country. A manager may want to know which countries they should promote more in. Knowing which countries generate the most revenue, may also give the manager an idea of what regions they should expand the platform to.
<img width="1146" alt="Screenshot 2025-03-15 at 7 54 58 PM" src="https://github.com/user-attachments/assets/6e55a42c-6ab6-489a-a005-cd583e750e76" />





3. This query retrieves a user’s complete billing history, including total subscriptions and amount spent. This can help Letterboxd to track user subscription behavior. It helps in identifying loyal customers who upgrade plans, users who downgrade, and potential customers who might leave the platform.
<img width="1152" alt="Screenshot 2025-03-16 at 11 12 49 AM" src="https://github.com/user-attachments/assets/81c1a7e8-c124-465b-b46e-6cc7c7618fbe" />




4. This query presents the director who has directed the most movies in our database. Useful for analytics on popular filmmakers within Letterboxd’s dataset. This information can enhance search recommendations and be used for content curation.

<img width="1200" alt="Screenshot 2025-03-17 at 12 37 08 PM" src="https://github.com/user-attachments/assets/3c9911d7-7991-4fb6-b721-c2243efb3b4e" />



5. Query 5 presents the number of users per subscription tier, there are three tiers comprising of free, pro, and patron. This can analyze the popularity of different subscription tiers and evaluate pricing strategies. If too many users are on the free tier, Letterboxd may need incentives to push users toward paid tiers
  <img width="832" alt="Screenshot 2025-03-17 at 12 47 27 PM" src="https://github.com/user-attachments/assets/72b75f68-4197-4ebe-9b72-9ad03fc25025" />




6. This query presents Users who have left more than 2 reviews and have had their account since January 5th. This can identify highly engaged users who actively contribute content to the platform. These users might be targeted for loyalty rewards or community-building efforts.


<img width="878" alt="Screenshot 2025-03-17 at 12 48 12 PM" src="https://github.com/user-attachments/assets/2df15a3e-1375-46ec-8430-2a704361ea3a" />





7. Query 7 displays the most reviewed movies released in the 70s. A manager may want to know this information to see what movies they should collaborate with for merchandise and other items to draw in more customers.
<img width="754" alt="Screenshot 2025-03-17 at 12 59 51 PM" src="https://github.com/user-attachments/assets/591b362d-ad62-472e-85bd-d4c48ff51711" />

8. Query 8 displays the times that users are active, ordered from most to least active. A manager may use this information to see what times are the best for sending out any promotional or informational emails and notifications.

<img width="1144" alt="Screenshot 2025-03-17 at 1 25 56 PM" src="https://github.com/user-attachments/assets/1615ae9a-14ac-4ebe-b07e-0be736a81a2a" />

   ## Database Information
Database Name: ns_Sp25_21479_Group6

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
