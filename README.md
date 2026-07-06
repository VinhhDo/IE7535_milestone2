Northeastern University

IE7500

Prema Parks, Vincent Do

Financial websites in original dataset blocked our automated scraping tools, we manually collected the article text for this submission. 
The project pipeline is fully built to handle this text now, and we will extend the dataset with more URLs later.

## 📌 Project Model Development Overview

Manually tracking earnings reports and market updates across dozens of live links is inefficient. This tool automates the entire text processing lifecycle:
1. **Data Ingestion:** Reads source URLs dynamically from an Excel file tracker.
2. **Web Scraping & Cleaning:** Extracts clean, relevant text from target web pages while bypassing HTML noise.
3. **NLP Aggregation:** Passes clean text into a custom summarization model.
4. **Sentiment Analysis:** Flags market sentiment for posive, neutral and negative.
  
  
## 📌 Research and Selection of Methods

The purpose of this project is to summarize lengthy financial reports into concise briefings to make them easier for people to read, thus making them more accessible. 
  The project will use NER to identify stock symbols, companies, and financial indicators, as well as a sentiment analysis to classify the news as positive, negative, or neutral. 
  We are building our system using methods similar to the ones used in the FinBERT study (Araci, 2019). Like in the study, we will be using a specific financial news dataset so 
  that our model is able to understand the industry terms better. In addition, we will use training techniques from the research to ensure the model is able to retain language skills 
  while it learns to summarize financial news. Finally, we will also use ‘transfer learning’ to make sure the AI is accurate to minimize the amount of data needed. Furthermore, research shows 
  that FinBERT consistently outperforms general purpose models like BERT and maintains high accuracy when training data is limited (Huang et Al, 2022). 
  
For our baseline summarization model, we used the facebook/bart-large-cnn transformer from Facebook Research (Lewis et al. al, 2020),  which was originally trained on the CNN/DailyMail dataset 
  for abstractive summarization. We tested this model on the following excerpt from an economic news release from the U.S Bureau of Labor Statistics: “The index for food rose 0.2 percent in May 
  after rising 0.5 percent in April. The food at home index increased 0.1 percent over the month… the index for limited service meals rose 3.3 percent over the same period.” (Consumer Price Index Summary). 
  The model provided the following summary: “Three of the six major grocery store food group indexes increased in May. The index for food rose 0.2 percent in May after rising 0.5 percent in April. 
  The food at home index increased 0.1 percent over the month. In contrast, the index for dairy and related products fell 0.6 percent. “ This model misses some of the key data from within the original excerpt; 
  however, we believe training our data on a financial dataset will greatly improve the accuracy of the summary. In addition, we have our model produce a longer summary as this particular model has been trained 
  that a good summary is a certain number of words long. Financial articles tend to be more verbose than the data this model was trained on, so this will help account for the loss of information. 

In the future for this project, our dataset will include more examples, and we are working through fine tuning our classification methods. 


