# Chapter 10
## 10.1 Motivation
In modern world we need to collect enormous amount of user generated data:
- what pages do they use?
- what do they buy?
- ...

Traditional relational databases are not well suited for Big Data, because:
- Volume
    - The amount of data is much larger than in traditional relation DB
- Velocity
    - The rate of arrival of data is high
- Variety
    - The structure of Big Data is too different from relational 

### 10.1.1 Sources and Uses of Big Data
Web companies realised that there are a lot of reasons to collect user data:
- Helps to understand which ads to show
- Helps to understand what posts, views and etc. show to user
- Helps to understand how to design the site
- Helps to determine current trends. What to produce/manufacture?
- Helps to collect `click-through` and `conversion` information
    - `click-through` - how many users clicked on the ads
    - `conversion` - how many users did the desired activity (e.g. bought something after watching ads)

Nowdays, there are many other resuorces of high-volume data:
- Data from mobile phone apps
- Transactions data from enterprises (both online and offline)
- Data from sensors. 
    - Monitor health of equipment
- Metadata from communication networks. E.g. traffic

Companies pay specialists to track the response of users to new products/ads. If the response is bad, the company want to cancel the product production/ads as soon as possible.

`internet of things` - a network of physical devices, vehicles (e.g. public transport), appliances, and other physic objects that are embedded with sensors, software and network connectivity, allowing them to collect and share data.

parallel storage - method of storing data across multiple storage devices or nodes simultaneously to improve perfomance, reliability, and scalability.

### 10.1.2 Querying Big Data
Since relational databases are not the best variant for Big Data there are some alternatives
1. Transaction-processing systems that need very high scalability.
    - Large number of short-running queries and updates
    - key-value storages are the best variant
        - no `JOIN` (like in SQL) but allow to join data by keys. Example, user U0 made a post, user Ui friend of U0 should receive notification. So, we go to user U0 and get his friends' keys, then we find friends by this keys and add info that U0 made a post. 
2. Query processing systems 
    - need very high scalability, and need to support non-relational data 
    - Data is often stored in multiple files, requiring systems to manage large files and support parallel querying.

