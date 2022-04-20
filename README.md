# Reduce The Noise Of News Search
**Contributers and Contact Information: [ ]**
1. AMANI Kouakou Noé,leader (+225 0142662716, kouakounoeamani1@gmail.com)
2. Tuo Navigué (+225 0759190122, navigue.tuo229@gmail.com)
3. Eloiflin Damo (+225 0767516289, damoeloiflin@gmail.com)
4. Blé Yatana Jean De Dieu (+225 0789454253, blejean2930@gmail.com)

**Problem Statement addressed :  

- Google, while a wonderful resource for quick-fix questions, starts to repeat search results after the third page, this is especially true for news articles. A big reason for this is duplicate resources from common sister agencies like Associate Press and all the newspapers that use its articles, as well as reshares or reposts, artificially inflate the volume of an article/post and its importance. Re-posts or re-shares often are also changed slightly so Google does not see them as duplicates. 
- This causes inflated importance of some posts (going “viral” unnecessarily) and gives a noisy Google search experience that may be hiding more relevant news articles from end-users.


**Description**: 

What our project is trying to accomplish here is that News articles with the same content are identified and associated with each other in order to prevent inflation of information importance. Attempt to identify duplicate news articles that we scrape from Google or internet search results and what sources those articles commonly come from. This information is used to better enable the public to make sure they're getting the most important and diverse information.

Therefore we are able to do those things with tigerGraph : 
1. Identify duplicates in a static news dataset in the graph,
2. Identify if a new article is a duplicate of an existing article in the graph, 
3. Enable others to use the similarity model on news datasets, and
4. Allow for a search engine to traverse the graph and retrieve the hyper-node (and the articles/posts it relates to) for retrieval and display

To do so ,we took 30-50 news articles and posts (even distribution if possible) and create a hypergraph of as many duplicate or near duplicate articles .Then,we assessed the metadata for duplicate information to create a similarity score, the most similar articles/posts  create the cluster of articles/posts related to each hyper-node. We decided the threshold for similarity which is over 80% (0.80 f-score) similarity on metadata fields . Representing the similarity of metadata between hyper-nodes allows for the solution to scale so that as new news articles/posts are posted, the metadata can be queried to identify if the new article/post is an existing duplicate, or a new article/post.

				

- Impactful in solving a real world problem 

On average, the typical internet user will search Google 4 times a day. Based on these figures, the number of people using Google search daily has been estimated at roughly 1.7 billion – considering there are 7 billion daily searches. (Source: 99firms.) So solving an issue on this platform may touch many users around the world.

- Innovative use case of graph

Using the fastest tool which is tigerGraph to better enable the public to make sure they're getting the most important and diverse information is one the innovative solutions we ever seen in this world.

- Ambitious and complex graph

Our solution takes less time to find the best information ,highlighting copyright and fight against "fake news" because it goes to the root of the information and then verifies the author .

- Applicable graph solution 

The machine learning model is open-source on Github and is flexible enough to be pointed at any news dataset that has standard metadata such as Google News or social media news feeds like Twitter, and allow for the similarity threshold to be modified.


Other additions: 

 - **Data**: 

 We retrieved 100 articles through general news API that we cleaned and prepared for our model.You can find the dataset in this file (csv format). 

 - **Technology Stack**:
 1. tgcloud.io : the plateform we used to build the graph and train the model
 2. newsapi.org : this is where we took the data
 3. python : we used it to treat the excel file
 4. gsql-language : the graph sql for queries in tigerGraph to get information from our data
 5. gsql-graph-algorithms : AI graph we used according to our needs

 - **Visuals**:
 - [demonstration] https://www.youtube.com/watch?v=GVl-a1p6oG8

## Dependencies
None

## Installation

1. Clone repository
2. Donwload the zipped file **export_4538711112.tar.gz** in the src folder
3. Upload it to tgcloud.io
4. load the csv file **data_tesla_2.csv** and **relation_graph.csv** located in the src folder
5. Run Queries such us identifying duplicate articles

## Known Issues and Future Improvements

We are developing something like Google scholar or connected papers to make our solution more useful for users.
The more articles there are, the more time the system takes to build the graph, but this is not a big problem because TigerGraph handles it.

## Reflections

In order to carry out our project we followed some strategic plans which were really helpful :

1. We first analyzed some issues that affect the whole world and then we brainstormed.
2. So we decided to look into Google, as it affects users around the world.
3. We then found a way to solve the problem with tigerGraph
4. We had a privilege to attend a TigerGraph training (2 days) orginized by SaH Analytics International (https://www.linkedin.com/company/sah-analytics-international/) and delivered by Mr Hanif Ullah Khan, Data engineer and TigerGraph Analyst in order to handle the tool.
5. We finally started working on the implementation and got ready to show the result to everyone.

## References
- [articles] https://newsapi.org/
- [tigerGraph] https://tgcloud.io/
- [gsql-graph-algorithms] https://github.com/tigergraph/gsql-graph-algorithms
- [Similarity-data-science-in-Tiger-graph-resources]  https://info.tigergraph.com/hubfs/Graph%20+%20AI%20World/Graph-AI-FPGA.pptx.pdf and https://www.tigergraph.com.cn/wp-content/uploads/2021/04/EN_OReilly-book-Grah-powered-Analytics-and-Machine-Learning-with-TIgerGraph-Early-release-April-2021.pdf

