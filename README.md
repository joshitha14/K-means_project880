# Project880

**Title**
Determining the Security Behaviors of Election Pollworks: Clustering and Unsupervised Learning of SEBIS Data


**Project Description**
In 2017, the Department of Homeland Security (DHs) designated elections infrastructure as critical infrastructure, and an overlooked component is the nearly 1,000,000 poll workers that are charged with ensuring the integrity of votes and security of voting equipment at the state and local level. Poll workers are on the first line of defense in elections security and are trusted insiders to the process. 

In this project, I shall take advantage of the dataset that comprises of 2,213 poll workers Security Behavior Intentions Scale (SEBIS) survey responses which were collected during a campaign in spring and summer 2020 targeting previous poll workers and those who intend to serve in the 2020 General Election and yielded over 2,2000 viable survey responses from 13 states. 

With the provided non-labelled dataset, I shall utilize jupyter notebook to implement and efficient K-means clustering algorithm in the Python language and then use the clusters formed as the labels to train the Support Vector Machine (SVM) model to predict and determine the poll workers security behaviors and their impact on election security. I will explore a few metrics, like Silhouette co-efficient, Calinski Harabaz Index, Fowlkes Mallow Score and Adjusted Rand Index Score to evaluate the results of the algorithm using Tensorboard, which enables tracking experiment metrics and visualize the results.

**ANALYSIS OF RESULTS
From below figures and based on the analysis from the clusters Excel file in the GitHub, Cluster 1 and Cluster 2 have highest number of people who are above 50. Additionally, Cluster 1 and Cluster 2 has people with more experienced, who are extremely comfortable in using the laptops. Essentially, pertaining to SEBIS questions Cluster 1 and Cluster 2 have significantly greater number of people (ranking wise) who lock their systems (Device Securement); who use different passwords for different accounts (Password Generation) and has greater number of people who never click a link when someone sends it (Proactive Awareness) and greater number of people who verify their Anti-virus software is regularly updating itself. On the contrary, Cluster 0 and Cluster 3 have a greater number of people who has degree lower than the associate degree. Also, has the highest number of people who do not lock their systems manually or do not auto lock their systems (Device Securement); who do not set their passwords to their mobile phones (Password Generation). This work concludes that poll workers who have higher education, who are above 40 years of age and who are extremely comfortable in using the computer or laptops has highest number of poll workers (ranking wise) who lock their systems, who use different passwords for different accounts and who never click a link when someone sends it. Moreover, these people update their software or anti-virus up to date. Precisely based on this analysis, gender or the age may not be accurate because a greater number of females have taken this survey, and furthermore, there are almost 310 people who are above 40 years of age. So, this work had to just consider the analysis based on qualification and level of comfortability in using the computer.

![Screenshot 2024-09-12 at 9 51 44 PM](https://github.com/user-attachments/assets/142f70ef-2c47-447d-90c4-003d32695d95)
![Screenshot 2024-09-12 at 9 51 50 PM](https://github.com/user-attachments/assets/e3f5547b-5f67-4863-a790-f9705f626e2c)




![Screenshot 2024-09-12 at 9 47 16 PM](https://github.com/user-attachments/assets/974cdf97-5cdc-4cb4-b9f4-52bfdca5a2f9)
![Screenshot 2024-09-12 at 9 46 56 PM](https://github.com/user-attachments/assets/eb7829a7-da09-4965-ae2f-7b59499cb8d3)
![Screenshot 2024-09-12 at 9 46 26 PM](https://github.com/user-attachments/assets/421fba21-8476-48ad-8ec2-ec44ada9d29d)
