![image](https://user-images.githubusercontent.com/26519123/120105902-1a28d380-c15b-11eb-8221-ec55f238bc3b.png)

# 1. SENTIMENTS



```
#!pip3 install vaderSentiment
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

analyzer = SentimentIntensityAnalyzer()
r1 = analyzer.polarity_scores("I don't like the movie")
r2 = analyzer.polarity_scores("I hate the movie")
r3 = analyzer.polarity_scores("I like the movie")
r4 = analyzer.polarity_scores("I love the movie")
print(f's1 = {r1} \ns2 = {r2}')
print(f's3 = {r3} \ns4 = {r4}')
```
```
s1 = {'neg': 0.345, 'neu': 0.655, 'pos': 0.0, 'compound': -0.2755} 
s2 = {'neg': 0.552, 'neu': 0.448, 'pos': 0.0, 'compound': -0.5719}
s3 = {'neg': 0.0, 'neu': 0.545, 'pos': 0.455, 'compound': 0.3612} 
s4 = {'neg': 0.0, 'neu': 0.417, 'pos': 0.583, 'compound': 0.6369}
```


# 2. INTENTS

# 3. NER

