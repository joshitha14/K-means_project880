# Project880

**Title**
Determining the Security Behaviors of Election Pollworks: Clustering and Unsupervised Learning of SEBIS Data


**Project Description**
In 2017, the Department of Homeland Security (DHs) designated elections infrastructure as critical infrastructure, and an overlooked component is the nearly 1,000,000 poll workers that are charged with ensuring the integrity of votes and security of voting equipment at the state and local level. Poll workers are on the first line of defense in elections security and are trusted insiders to the process. 

In this project, I shall take advantage of the dataset that comprises of 2,213 poll workers Security Behavior Intentions Scale (SEBIS) survey responses which were collected during a campaign in spring and summer 2020 targeting previous poll workers and those who intend to serve in the 2020 General Election and yielded over 2,2000 viable survey responses from 13 states. 

With the provided non-labelled dataset, I shall utilize jupyter notebook to implement and efficient K-means clustering algorithm in the Python language and then use the clusters formed as the labels to train the Support Vector Machine (SVM) model to predict and determine the poll workers security behaviors and their impact on election security. I will explore a few metrics, like Silhouette co-efficient, Calinski Harabaz Index, Fowlkes Mallow Score and Adjusted Rand Index Score to evaluate the results of the algorithm using Tensorboard, which enables tracking experiment metrics and visualize the results.
