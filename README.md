# Pickit - Smart Grocery Basket
## “A Fastrack for Shopping”


### Problem Statement :- 
A prototype, Pickit, that identifies grocery items and recommends items based on prior purchase history and providing item location.

### Significance and Proposed Scope :-
Smart Grocery Detection is essential to a grocery store's capacity to manage its workforce effectively. Real-time information on item availability is needed to 
determine when to redesign or replenish an item. As a result, the customer can always find the item on the rack when they need it. This study focuses on managing 
product displays at a grocery shop to decide how much of a specific product to stock on the shelves.
1. There are lot of limitations with the ordinary grocery stores and online delivery stores, we propose a model which can solve much of these limitations.
2. Most of the time even though there are number of salespersons, the user finds it difficult to locate the product in a grocery store. Sometimes the crowd in the store interacting with salespeople makes it difficult for other users in the shop. Moreover, it creates an unfriendly environment sometimes. Also, people from out of the state finds it difficult to communicate with salesperson. Our model can give the user the location of items.
3. ‘Time is money’ -usually a lot of time is wasted searching for the products in grocery stores and even if it is from an online store, there are chances for 
unpredictable delays. Our proposed model ensures no wastage of time as one can select items easily within a short span of time.
4. Once we are trying to shop things online, when we select a grocery item there aren’t many apps which recommend other products based on our selected item, i.e., if we are selecting items for breakfast -if we select bread, it won’t recommend items related to it like egg or milk, our model could recommend items based on the items we have taken first.
5. When users want to order a lot of items ,there is a limit or orders in online shopping and it won’t be practical in case of bulk orders and if we are buying from an ordinary store, there are chances users might forget some items to buy .If a user uses our model, even if the user remembers some of the items to be bought, our model could recommend other items which are in high correlation with it, so one don’t need to remember all the items to be bought.
6. People prefer online stores to ordinary stores nowadays because of the time wastage and difficulty for selecting items in ordinary store, even though ordinary stores are perfect for quality check. Our model ensures good quality products within the shortest span of time.
“Prefer Normal to Pareto-the high standardized grocery shops have good partnership deals with the renowned online delivery apps and they get good market from online trade too. The local retailers find it difficult to compete with the higher class. Our model could be helpful to this class of people and making the middle-class people get better would be preferable than making the rich richer. It could be beneficial for the economy of country as well”


### About Dataset :-
The image dataset which we collected comprises of 50-50 images each of the products in various categories. These products include: -
1) Bread
2) Butter
3) Eggs
4) Coconut
5) Milk

![image](https://user-images.githubusercontent.com/81613474/194701098-124b662c-c830-47ab-952b-4cb086d251d8.png)
![image](https://user-images.githubusercontent.com/81613474/194701114-94e556f9-10e9-4881-9cc4-9b4b9a0162c2.png)

Through Web Scrapping we got one folder at once which contains all the images.

### 3D Grocery Store :-
Since the project mainly focusses on product detection in grocery store, it was necessary to build a layout of how a grocery store looks. So first we made a rough sketch of a grocery store on a paper.Then we wanted to build a 3D model of that grocery store so that we can see and visualize the store to make our process and workflow easier. For that we used Blender to create our 3D model of grocery store.

![image](https://user-images.githubusercontent.com/81613474/194701254-d7aac6ae-92b1-4c9f-86ae-1ad295ff2620.png)
### Methodology :-
1)Object detection
  Here, we developed a model so that customer will select a product in grocery store and scan it and then the model detects that specific item.
  What is Robo flow?
  Robo flow is a Computer Vision developer framework for better data collection to pre-processing, and model training techniques. Robo flow also offers the option to create a dataset using a split that the user defines.
  1) Pre processing
    In pre-processing, there was inbuilt feature in Roboflow for giving annotations. We put labels on each of the photos. Along with this, Roboflow increased our dataset by rotating every image with different angles. So, now we have approx. 2000 images as compared to earlier where we have 720 images
  2) Data Production
    In this process, Roboflow divided our dataset into three folders, that is, TrainingTesting and validation. In each of these folders, there were 2 subfolders- images and labels. Data.yml files extracted all the labels which we gave and then allotted respective labels on respective itemsAfter processing the dataset from Robo flow we got 1 API key and then used that to import data in yolo for further detection.
  What is Yolo?
  YOLO is one of the most famous object detection algorithms due to its speed and accuracy.
  We used YOLO V5 which is model trained on COCO dataset and which uses a transfer learning technique. We tuned this model on our dataset to get better accuracy for object detection.


2)Object Recommendation
  We made a model trained on the real time dataset of a store which has the combinations of products customers are buying. It recognises the buying pattern of customers and recommending the most likely product that a customer can buy next.
We developed this model using two techniques:-
  1) Association rule
    Large volumes of data are analysed using association rule mining to uncover intriguing linkages and relationships. This rule displays the number of times an itemset appears in a transaction. An example of this is a market-based analysis.
  2) Apriori Algorithm
    Apriori algorithm refers to the algorithm that determines the rules of association between items. It refers to the relationship between two or more objects. To put it another way, we can say that the apriori algorithm is a leaning association rule that examines whether customers of Product A also purchased Product B.
  How the Pickit Recommendation system helps?
  Using this information, retailers can design promotions for their goods, such as providing a discount on the best rules or tying a free item to the number of best associated rules that buyers purchase collectively. In either scenario, buyers wind up paying more money in order to take advantage of these discounts. As a result, the company experiences great profit as well as high sales.
