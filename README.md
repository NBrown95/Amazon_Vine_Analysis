# Amazon Vine Analysis

## Overview of Project

For this project, we are analyzing Amazon reviews written by members of the paid Amazon Vine program. This program is a service that allows manufacturers and publishers to receive reviews for their products. For this analysis, we are looking at a dataset of reviews for wrist watches. We then used PySpark to extract and transform the data. Then we connect to an Amazon Web Services RDS instance and load the transformed data into pgAdmin. We then used PySpark to determine if there was any bias toward favorable reviews from Vine members for wrist watches. 

## Results

Three questions that we wanted to answer were how many of the reviews of wrist watches were written by Vine members vs Non-Vine members, how many five-star reviews were there for the wrist watches, and the percentage of five-star reviews for both Vine reviews and Non-Vine reviews.

### Vine vs Non-Vine Reviews 

The screenshot of the total number of reviews is below.

![Screenshot 1](https://user-images.githubusercontent.com/81498850/128617338-e74bc722-3b87-4e89-b4d6-086cb8e297da.png)

As we can see, the vast majority (around 99%) of reviews for wrist watches were written by Non-Vine members. This makes it difficult to find any bias in Vine members’ reviews because the sample size is so small.

### 5-Star Reviews 

The screenshot of the total number of five-star reviews is below.

![Screenshot 2](https://user-images.githubusercontent.com/81498850/128617349-e2c0a19a-fc38-4eb4-9f6a-adcd64de212f.png)

Based on this information, we can see that because the sample size was so small for Vine members, it appears that the number of five-star reviews is very rare for that group. To determine if this number is proportionate to the Non-Vine members’ group, we must look at the percentage of reviews that are given five stars for each group and compare them. 

### Percentage of 5-Star Reviews 

The screenshot of the percentages of five-star reviews is below.

![Screenshot 3](https://user-images.githubusercontent.com/81498850/128617354-b1ca95fd-4774-4e3c-883e-05ca230c4efd.png)

As we can see, the percentage of reviews from Vine members that were given a five-star rating was less than one-third at around 31.9%. However, the percentage of reviews from Non-Vine members that were given a five-star rating is over half with 51.8%. This tells us that non-Vine members actually gave higher ratings per review than Vine members. 

## Summary 

Based on these results it is difficult to reject that there is bias in Vine members’ reviews. This is simply because the sample size is so small that it is not sufficient to conclude the results are representative of all Vine members. However, we found that non-Vine members give more five-star ratings per review than Vine members. Therefore, we cannot say there is positivity bias. 

One reason for our finding could be that these Vine members write more critical reviews as they take their role seriously as paid review writers. Therefore, they are looking for reasons to not give a five-star review to help these companies with helpful, constructive feedback. However, we cannot conclude that this is happening based on this data.

An additional analysis that would support this theory would include looking at the length of the written reviews and comparing them between groups. If the Vine members were writing more critical feedback, then their reviews would presumably be longer than the average non-Vine member who has no monetary incentive to write long reviews. 
