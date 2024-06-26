# Repository - Analysis

### This repository contains code analysing a limited set of reviews left by customers for Apple AirPods to glean some data relating to consumer preferences. <br>

<br>
<img src="https://images.unsplash.com/photo-1713492527322-471061e52516?w=900&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Nnx8YXBwbGUlMjBlY29zeXN0ZW18ZW58MHx8MHx8fDA%3D" alt="alt text" width="300"/>

<br>

### Objective- To analyse topic prevalence within the reviews and identify whether members of the Apple ecosystem are more likely to leave a positive review than non-members.

### INTRODUCTION-
Insights into consumers' opinions about a product is vital in product improvement. In this limited experiment, I aim to analyse a small dataset of reviews left by Apple AirPods users. The data is segemented based on how long the customer has used the product. <br> 
The dataset has 2 broad categories of reviews- <br>
1. Reviews mentioning the Apple ecosystem <br>
2. Other reviews, which for the purpose of this analysis, have been considered to be reviews left by customers who do not place importance on the product's integration into the Apple ecosystem <br>


I will pick out some key topics mentioned in the reviews, and create a heatmap which explores the prevalence of said topic within each dataset as well as the combined dataset. <br>
<br>
I also test a small hypothesis that members of the Apple ecosystem are more likely to say positive things about the AirPods. **Will this hold true?** <br>
#### Data structure - <br>
The scraped data looks like this- <br>
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/Data%20structure.png" alt="alt text" width="1000"/>
#### Exploratory Data Analysis 1 - Average Ratings

I wanted to explore whether members of the Apple ecosystem would be more likely to be critical or supportive of Apple AirPods<br>
The analysis revealed that the average rating left by members of the Apple ecosystem was 2.5% lower than that of non-ecosystem members.
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/RatingDistribution.png" alt="alt text" width="800"/>

| User Type | Average User Rating |   |
|---|---|---|
| Ecosystem Member | 4.71 out of 5 | ☹ |
| Other | 4.83 out of 5 | ☺ |

<bold>VERDICT FOR HYPOTHESIS: Does not hold true! </bold>
<br>
#### Exploratory Data Analysis 2 - Word Count Plot

I wanted to quickly visualise the most common words used within the 2 datasets, and hence, have created Word Count Plots where the size of the word shows its prevalence

1. Ecosystem Reviews- <br>
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/WordCountPlotEcosystemReviews.png" alt="alt text" width="800"/>
<br>
2. Other Reviews- <br>
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/WordCountPlotOtherReviews.png" alt="alt text" width="800"/>
<br>
#### Exploratory Data Analysis 3 - Heatmap of common words

To get a more granular look on what members of the ecosystem versus others talk about relating to the Apple AirPods based on how long they've used the product
There are 4 buckets of product usage -
1. Less than 1 month
2. More than 1 month but Less than 6 months
3. More than 6 months
4. Unknown (Data Not Available)

Common words were ignored, and 25 other highly prevalent keywords were selected.

The two data aspects which were looked at together were-
1. Product age at the time of review (Bucketed)
2. Keyword

Results looked like this-
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/AirPodsStaticHeatmapEcosystemReviews.png" alt="alt text"/> <br>
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/AirPodsStaticHeatmapOtherReviews.png" alt="alt text"/> <br>
<img src="https://github.com/kirtanag/analysis_apple/blob/main/images/AirPodsStaticHeatmapOverallReviews.png" alt="alt text"/> <br>

(Note: While the heatmap below is static, it can be interacted with here: 
### https://kirtanag.github.io/analysis_apple/AirPodsInteractiveHeatmap.html

### CONCLUSION-

A. Based on EDA 1, we know that members of the Apple ecosystem are around 2.5% more likely to give a lower rating to Apple AirPods than others.

B. Based on EDA 2, we see some words being used very frequently across the datasets. They are- <br>
[i] Ecosystem reviews - **Ecosystem, Product, Sound, Quality** <br> 
[ii] Other reviews - **Use, Quality, Easy, Sound** <br>

Some key conclusions from it include: <br>
[a] Overall, a lot of users talk about the product's sound quality, as well as phone (presumably about connecting to their phone) <br>
[b] More people talk about how the AirPods work more than 6 months into using it. <br>
[c] There is a non-trivial downward movement of the mention of quality in the overall heatmap as time progresses. <br>
[d] Unsurprisingly, members of the ecosystem talk about sound quality more than other reviewers. <br>
