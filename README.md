# ADM_HW4
Hello everyone!!
So this is our repository!! 
For now, as said today in whatsapp:
Zhibek:
 
You are on this task!

2) Find the duplicates!
You are given passwords2.txt file as input. Each row corresponds to a string of 20 characters. Define a hash function that associates a value to each string. In this case, the goal is to check whether there are some duplicate strings. Our definition of duplicate is that the two strings have the same characters, order is not important. Thus, "AABA" = "AAAB".


There are 3 steps that you need to perform:

1)Convert the string containing the password to a (potentially large) number

2)Use a hash function to map the number to a large range. Read the class material and search the internet for this part (but you need to write the code yourself).

3)After having defined the hash function, find if two numbers fall on the same range

In the file there are 10M duplicates, can you detect them?
Does it happen that two strings with different characters are hashed to the same value? If yes, could you provide the number of False Positive?

Now do the same thing as before, but now the order of the characters must be put into account. Example: "AABA" != "AAAB".


Me and Valerio:

2)
Goal
You will implement two clustering and compare the results you get. You will need to create two datasets and each of them will be filled by data that you scraped.

*Scraping*  <----at the moment we are at this step


This time, you must create your dataset. The website that you will scrape is: here. In particular, you should retrieve at least 10k announcements starting from this link. The information that you need to extract is explained afterwords. Remember, whenever you have text to work on, do some pre-processing. Use the Beautiful Soup library to parse the html. 

Make sure to put a time.sleep(t), where t is the number of seconds, to prevent the website block. It might take a while, be patient.
Datasets

1) Information
The first matrix will have this format:  where  and . n is the number of the announcements. It's possible that not all the announcements will have all the fields mentioned above, if it's the case don't take it into account. (look at cristina's file)


2) Description
The second matrix will have this format:  where  and . n is the number of the announcements and m is the cardinality of the vocabulary. This time, you must implement the Tf-Idf by yourself (not with libraries). Make sure to use the complete description inside the link of the announcement: example. (look at cristina's file)


Clustering
This step consists in clustering the house announcements using K-means++. In order to do that you can use this Python library. Choose the optimal number of clusters using the Elbow-Method.



Comparison among cluster
We expect that both datasets will lead to similar clusters. Is this true?
Find similar clusters

To check this, use the Jaccard-Similarity to measure the similarity betweeen the two outputs (information clusters vs description clusters). Return the 3-most similar couples of clusters.
Word cloud of house descriptions

With this last output you must create a wordcloud for each couple of clusters. The words that will be represented are those extracted from the description of the houses that are in the relative couple.

we will work on this :)

ps: now we don't take into account the bonus part 
