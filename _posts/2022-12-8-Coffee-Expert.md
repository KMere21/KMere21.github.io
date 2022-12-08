---
layout: post
title: Capstone Followup - Conversation with a Coffee Expert
date: 2022-12-8
preview: true
---

While I enjoy great coffee and researched some background for my capstone project “Predicting Coffee Ratings from Expert Reviews”, I am not a coffee expert. Therefore, I wanted to follow up with someone from the industry to see what they thought of my findings. [Olivia Auell](https://www.linkedin.com/in/oliviaauell/), sensory scientist and coffee expert, graciously agreed to chat (full disclosure, we are friends from college). 

## The Source Data

Given the importance of data quality in any data project, we discussed the source data (including its limitations) before getting into the findings. The data was pulled from [Coffee Review](https://www.coffeereview.com/). The reviews were conducted by a small team following the standardized Specialty Coffee Association of America protocols, which are globally highly regarded (note, SCAA is now merged with a European association to form the [SCA](https://sca.coffee/about)). However, as the [reviewers acknowledge](https://www.coffeereview.com/how-coffee-review-works/), coffee taste preferences are fundamentally subjective. Olivia brought to my attention that the SCA is working to address this by [piloting revisions](https://sca.coffee/sca-news/read/evolving-the-sca-cupping-protocol-and-form-an-overview-of-the-pilot-testing-process) to their protocols. These revisions will account for changes in the specialty coffee industry and incorporate new insights from sensory science. 

We also discussed some issues with the measurement process. Olivia pointed out that the review process assigns numbers, but that those numbers then are really representing a qualitative assessment, such as ‘this is excellent’, ‘this is good’, etc.). You can see how Coffee Review intends the overall score to be interpreted [here](https://www.coffeereview.com/how-coffee-review-works/).

Finally, Olivia also raised an ethical concern with the cupping system. Coffee scores historically have affected how much farmers are paid. Given the scoring system is still fairly subjective and catered to specific people’s taste (e.g. what coffee reviewer’s like does not always translate to what the average consumer likes), this can be problematic. However, this is starting to change. You can read more about this [here](https://sca.coffee/sca-news/25/issue-18/valuing-coffee-evolving-the-scas-cupping-protocol-into-a-coffee-value-assessment-system) and [here](https://static1.squarespace.com/static/584f6bbef5e23149e5522201/t/62ff6f82e076e71f661ca1c6/1660907395782/CVAS+Evolution+Report+2022.pdf).

## The Findings

One of the interesting outcomes is that despite some of the limitations of the source data discussed above, we can expect the final model to predict the overall score within one point of the actual score. Given overall scores range from 50-100, this is quite accurate. 

In addition, because the final version used a Lasso Regression model, it’s possible to get direct insight into which features of the review were important to the model for predicting the overall score. To do this, we look at the coefficients. Those left of 0 in salmon have a negative relationship with the score, meaning as they increase, the overall score tends to decrease. Those to the right of 0 in blue have a positive relationship with the score, meaning as they increase, the overall score tends to increase too. 

![_config.yml](/images/top_features_modeling.png)

### Feedback on the Findings

Generally, Olivia thought the findings made sense. While she was a bit surprised that flavor was as low as it was, the importance of first and last impressions (aroma and aftertaste) resonated from a sensory perspective. When tasting, one can become habituated to the taste. As the reviewer marks down scores, the aftertaste may still be lingering in the mouth.

Other areas where Olivia affirmed findings include:
* ‘Woody’ having a negative relationship with the overall score; this can often reference poor roasting
* ‘Flower’ having a positive relationship with the overall score; Gesha and many east African coffees have flower notes, both of which are anecdotally associated with high quality coffee
* ‘Cleanly’ having a positive relationship with the overall score; this probably refers to a clean cup, which is part of the evaluation process and typically characteristic of washed Arabica; a ‘clean cup’ is associated with high quality coffee

Interpreting a few of the other features and why the model found them important is less straighforward, including ‘almond’, 'guava', ‘hibiscus’, and ‘winey’. One reason is that terms can be used differently, so in an ideal scenario we’d have definitions from the reviewers. While Coffee Review provides a useful [glossary](https://www.coffeereview.com/coffee-glossary/), these terms are unfortunately not defined in it. 

Without a clearer understanding of their intended meaning, we are limited to speculation about these areas. Some of the potential explanations Olivia provided are as follows:
* ‘almond’ - Almond and cherry share the same aroma compound, they might be identifying this close relationship between the two
* ‘guava’ intrigued us both; this could be a reference to being acidic in a ‘mouth puckering way’ or having ‘biting acidity’; it could also be an indication of mouthfeel, not flavor
* ‘hibiscus’ - Hibiscus generally doesn’t have a strong aroma, so Olivia was curious about this one; we’d have to dig further to see if we can determine what they are referring to
* ‘winey’ - Winey could reference a lot of things; natural processed coffees tend to be more funky, like kombucha and have fermented notes; it could refer to mouthfeel or dark fruit aromas


## Conclusion

I really enjoyed chatting with Olivia about the findings and her expertise in coffee and sensory science. Our discussion affirmed some areas while also raising even more questions. Our discussion reinforced a few key aspects of working with and interpretting data:
* When possible, getting expert opinion is very important, especially when making recommendations that have real-world consequences. 
* Having shared definitions and understanding of terms is crucial for accurately interpreting findings. 
* This is of course only one study. Further research and examining other models would be useful to see if they find similar features important. Recommendations made from this should be taken with some caution. 
