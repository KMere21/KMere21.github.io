---
layout: post
title: Deploying an Interactive Data Application
date: 2023-2-1 
preview: true
---

During my data science bootcamp, we learned about [Streamlit](https://streamlit.io/), a really useful open-source app framework for deploying and sharing data projects. While working on my capstone, I used the tool to create a locally hosted app to demo my project. Now, I’ve created a version others can interact with! 

Learn more about the app and [try it for yourself](https://predict-coffee-rating.streamlit.app/)!

### Broader Applications: Model Preservation & Deployment

![_config.yml](/images/pickle_picture.png)

**Pickling** 

While this particular model has a narrow focus, the process of preserving a trained model and moving it into production is broadly useful. To move a model into production, I had to decide which model I wanted to use and then preserve it. In this instance, I wanted to use one of my text only models so that people could easily feed in new review text and see how it performed. After running training and validation data on various text models, I used the R-squared score to choose a promising model. 

Having done the project in Python, I then used “pickle” to preserve my model. This captures what my model learned from training data and allows it to be used in live applications. For more on pickling, check out Python’s documentation on pickling [here](https://docs.python.org/3/library/pickle.html).

The code to do this was surprisingly simple. Here’s a sample of what it looked like to save my model from the Jupyter Notebook (with “url_pathway” as a placeholder for the actual pathway). The "tfidf_final" and "final_model" portions are references to the model itself, run earlier in the notebook.

![_config.yml](/images/pickle_code.png)

**Streamlit**

My end goal was to create an interactive app that anyone could test out. Streamlit is perfect for this. Now that my model was in a pickle (.pkl) format, I could reference it in the application. I used example documentation for setting up a Streamlit app and customized it for my use case. Here’s what the section enabling the predictive model interaction looks like:

![_config.yml](/images/pickle_streamlit_code.png)

It was really rewarding to take my model from its “training grounds” in Jupyter Notebook and release it “in the wild” on Streamlit. I hope you enjoy testing it out!

*Photo Credit: Kristina Snowasp from Pexels*