# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Aim: 

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

# Explanation:

Develop a python code that integrates multiple AI tool by interacting with their APIs.
Compare outputs from different APIs.
Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

# SENTIMENT ANALYSIS

**positive review**
~~~
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

# Simulated AI-generated text
generated_text = "This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos."

print("Generated Review:\n")
print(generated_text)

# Sentiment analysis
sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

# Insight generation
if sentiment['compound'] > 0:
    print("\nInsight: The review is positive and suitable for marketing promotion.")
else:
    print("\nInsight: The review tone is neutral or negative.")
~~~

**output**
~~~
Generated Review:

This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos.

Sentiment Analysis:
{'neg': 0.0, 'neu': 0.556, 'pos': 0.444, 'compound': 0.8625}

Insight: The review is positive and suitable for marketing promotion.
[nltk_data] Downloading package vader_lexicon to /root/nltk_data...
~~~

**Negative review**
~~~
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

# Simulated AI-generated text
generated_text = "This smartphone is terrible and battery drain off shortly."

print("Generated Review:\n")
print(generated_text)

# Sentiment analysis
sia = SentimentIntensityAnalyzer()
sentiment = sia.polarity_scores(generated_text)

print("\nSentiment Analysis:")
print(sentiment)

# Insight generation
if sentiment['compound'] > 0:
    print("\nInsight: The review is positive and suitable for marketing promotion.")
else:
    print("\nInsight: The review tone is neutral or negative.")
~~~

**Output**
~~~
Generated Review:

This smartphone is terrible and battery drain off shortly.

Sentiment Analysis:
{'neg': 0.279, 'neu': 0.721, 'pos': 0.0, 'compound': -0.4767}

Insight: The review tone is neutral or negative.
[nltk_data] Downloading package vader_lexicon to /root/nltk_data...
[nltk_data]   Package vader_lexicon is already up-to-date!
~~~

# Result: 

Thus the prompt for both postive and negative review of sentiment analysis is exceuted successfully.



