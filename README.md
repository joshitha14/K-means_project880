# Project880

**Title
Determining the Security Behavior Intentions of Election Poll Workers: Clustering and Unsupervised Learning of SEBIS Data


**Project Description
In 2017, the Department of Homeland Security (DHs) designated elections infrastructure as critical infrastructure, and an overlooked component is the nearly 1,000,000 poll workers that are charged with ensuring the integrity of votes and security of voting equipment at the state and local level. Poll workers are on the first line of defense in elections security and are trusted insiders to the process. 

In this project, I shall take advantage of the dataset that comprises of 2,213 poll workers Security Behavior Intentions Scale (SEBIS) survey responses which were collected during a campaign in spring and summer 2020 targeting previous poll workers and those who intend to serve in the 2020 General Election and yielded over 2,2000 viable survey responses from 13 states. 

With the provided non-labelled dataset, I shall utilize jupyter notebook to implement and efficient K-means clustering algorithm in the Python language and then use the clusters formed as the labels to train the Support Vector Machine (SVM) model to predict and determine the poll workers security behaviors and their impact on election security. I will explore a few metrics, like Silhouette co-efficient, Calinski Harabaz Index, Fowlkes Mallow Score and Adjusted Rand Index Score to evaluate the results of the algorithm using Tensorboard, which enables tracking experiment metrics and visualize the results.

The main objective of this project is to identify the relationship between the extent of poll worker personal security practices and their impact on election security. Additionally, identifying the personal security practices that might impact polling place security and discuss how those results will impact the supply chain of votes and exploring the approaches outside of the election security The main step is to develop efficient k-means clustering and support-vector machine (SVM) models and to train the model. After training the model, the next step would be to evaluate the model and tune in the parameters to view the accurate results.

** EXPERIMENT
  - Data Preprocessing: To avoid the vast difference between the range of values, this work incorporated an important step in the analysis by standardizing the data. Standardization is an important part of data        preprocessing, and it comes to picture when features of input data set have differences between their ranges, or simply when they are measured in different measurement units. For this project, a Standard           Scaler was used to standardize the data.
    ![Screenshot 2024-09-12 at 9 57 31 PM](https://github.com/user-attachments/assets/bfe505f8-b488-426c-a573-0e2d95796394)
    After data standardization, dimensionality reduction is performed for which I have used Principal component Analysis, which is a very popular dimensionality reduction technique used to avoid “the curse of 
    dimensionality”.
  - Principal Component Analysis: Principal component analysis (PCA) is a method of compressing large data into something that captures the essence of the original data. PCA takes a dataset with lot of dimensions 
    (i.e., lot of cells) and flattens it to 2 or 3 dimensions, so we can look at it. It tries to find a meaningful way to flatten the data by focusing on things that are different between cells. Now, when plotting     a point based for each person behavior on how many reads were from each cell . PC1 (the first principal component) captures the direction where most of the variation is, and PC2 captures     the direction with     the 2nd most variation. PC1 and PC2 now becomes the new x and y axis
    ![Screenshot 2024-09-12 at 9 59 54 PM](https://github.com/user-attachments/assets/26399b88-2442-44de-8b58-87e818f35846)
    PC1 (the first principal component) is the axis that spans the most variation. PC2 is the axis that spans the second most variation. If we had 4 cells, PC1 would span the direction of the most variation, PC2       would span the direction of the 2nd most variation, PC2 would span the direction of 3rd most variation, PC4 would span the direction of the 4th most variation. There is a principal component for each dimension     (cell). If we had 200 cells, we would have 200 principal components. PC200 would span the direction of the 200th most variation. So, this work had to fit the standardized data (formed in Figure 11) using PCA
    ![Screenshot 2024-09-12 at 10 01 02 PM](https://github.com/user-attachments/assets/4529d275-5534-4634-890c-224c2271fabc)
    Secondly, how many features to keep had to be determined based on the cumulative variance plot, as shown in Figure 15. From the graph, the red line shows the cumulative sum, and we can read off the percentage      of the variance in the data explained as we add principal components
    ![Screenshot 2024-09-12 at 10 01 09 PM](https://github.com/user-attachments/assets/ae6bb995-d17e-4676-8026-6480f3cf1e84)
    we can see that the first principal component explains 15% of the variance of the dataset. The first 2 principal components explain 24% and first 3 explains 31%, first 4 components explain 38% and first 5          principal components explain 45% of the variance of the dataset. As the next step, this work performed PCA with the chosen number of components which is 5 principal components.
    ![Screenshot 2024-09-12 at 10 01 17 PM](https://github.com/user-attachments/assets/13d0f388-ae1a-4e82-bd2f-17023e4f2bd8)
    To perform segmentation based on principal components scores instead of original features is to incorporate newly obtained PCA scores in the K-means algorithm. So, to combine the PCA with K-means, it is            necessary to first determine the number of clusters to choose; to do so, the elbow method was utilized to determine the number of clusters

** Implementation
  - Next step was to run K-means with the number of clusters which is equal to 4. Subsequently we are fitting the model with the principal component scores
    ![Screenshot 2024-09-12 at 9 51 44 PM](https://github.com/user-attachments/assets/142f70ef-2c47-447d-90c4-003d32695d95)




**ANALYSIS OF RESULTS
From below figures and based on the analysis from the clusters Excel file in the GitHub, Cluster 1 and Cluster 2 have highest number of people who are above 50. Additionally, Cluster 1 and Cluster 2 has people with more experienced, who are extremely comfortable in using the laptops. Essentially, pertaining to SEBIS questions Cluster 1 and Cluster 2 have significantly greater number of people (ranking wise) who lock their systems (Device Securement); who use different passwords for different accounts (Password Generation) and has greater number of people who never click a link when someone sends it (Proactive Awareness) and greater number of people who verify their Anti-virus software is regularly updating itself. On the contrary, Cluster 0 and Cluster 3 have a greater number of people who has degree lower than the associate degree. Also, has the highest number of people who do not lock their systems manually or do not auto lock their systems (Device Securement); who do not set their passwords to their mobile phones (Password Generation). This work concludes that poll workers who have higher education, who are above 40 years of age and who are extremely comfortable in using the computer or laptops has highest number of poll workers (ranking wise) who lock their systems, who use different passwords for different accounts and who never click a link when someone sends it. Moreover, these people update their software or anti-virus up to date. Precisely based on this analysis, gender or the age may not be accurate because a greater number of females have taken this survey, and furthermore, there are almost 310 people who are above 40 years of age. So, this work had to just consider the analysis based on qualification and level of comfortability in using the computer.


![Screenshot 2024-09-12 at 9 51 50 PM](https://github.com/user-attachments/assets/e3f5547b-5f67-4863-a790-f9705f626e2c)




![Screenshot 2024-09-12 at 9 47 16 PM](https://github.com/user-attachments/assets/974cdf97-5cdc-4cb4-b9f4-52bfdca5a2f9)
![Screenshot 2024-09-12 at 9 46 56 PM](https://github.com/user-attachments/assets/eb7829a7-da09-4965-ae2f-7b59499cb8d3)
![Screenshot 2024-09-12 at 9 46 26 PM](https://github.com/user-attachments/assets/421fba21-8476-48ad-8ec2-ec44ada9d29d)
