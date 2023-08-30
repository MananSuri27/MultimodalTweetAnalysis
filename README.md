# MultimodalTweetAnalysis
This notebook represents our approach for Task 1B of the CheckThat! Lab at [CLEF 2022](https://sites.google.com/view/clef2022-checkthat/home). We ranked #1 on the task leaderboard on CodaLab.

<img width="620" alt="image" src="https://github.com/MananSuri27/MultimodalTweetAnalysis/assets/84636031/09d7fa11-6aac-4890-878a-65b867d93011">

## Task 1B
Verifiable factual claims detection: Given a tweet, predict whether it contains a verifiable factual claim. This is a binary task with two labels: Yes and No. This is a classification task.

## Methodology
### 1. Data Augmentation
We translated the Dutch and Bulgarian datasets for the task into English to increase the amount of training data we have.

### 2. Feature Extraction through Twitter API
We used the twitter API to extract the following data about a tweet:
1. Numerical Features:
- number of 'followers', 'following', 'posts' of the author of the tweet
- number of 'likes', 'retweets' of the tweet itself
3. Categorical Features:
-'verified' as an attribute of the author of the tweet
-'url' indicating presence of a URL in the tweet

### 3. Multimodal Model
We used the [Multimodal Toolkit](https://github.com/georgian-io/Multimodal-Toolkit) for text and tabular data with HuggingFace transformers as building block for text data.
