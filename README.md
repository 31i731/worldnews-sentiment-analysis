# Reddit Sentiment Analysis

## Overview
This project analyzes the sentiment of comments from the "worldnews" subreddit. The primary goal is to classify comments as either **Positive** or **Negative**, providing insights into how users react to global news topics. The dataset consists of comments scraped from Reddit using the PRAW Python library, focusing on posts from the past week.

---

## Project Steps

1. **Data Collection**:
   - Scraped the top posts and their comments from the "worldnews" subreddit using PRAW.
   - Saved main comments (excluding replies) for analysis.

2. **Data Preprocessing**:
   - Cleaned the comment text to remove unnecessary elements like URLs and markdown formatting.
   - Ensured punctuation and emojis were preserved to retain sentiment context.

3. **Sentiment Analysis**:
   - Used the Hugging Face model `siebert/sentiment-roberta-large-english` for sentiment classification.
   - Classified comments as either **Positive** or **Negative**.

4. **Results Visualization**:
   - Visualized sentiment distribution.
   - Highlighted top positive and negative posts based on comment sentiment ratios.

5. **Milestones**:
   - Saved the processed dataset with sentiment labels as a CSV file for future use in NLP.

---

## Dataset

### Data Source
- The dataset was collected using PRAW from the "worldnews" subreddit. Posts and comments were filtered to include only those from the past week.

### Fields in the Dataset
The processed dataset contains the following fields:

- **Post Title**: The title of the post.
- **Score**: The score of the post.
- **Comments**: A list of dictionaries, each representing a comment with the following fields:
  - `Comment ID`: Unique identifier for the comment.
  - `Comment Author`: Username of the commenter.
  - `Comment Content`: The text of the comment.
  - `Comment Score`: Upvotes received by the comment.
  - `Comment Created UTC`: Timestamp of comment creation (UTC).
  - `Sentiment`: Sentiment label (Positive or Negative).
- **Subreddit**: The subreddit from which the data was fetched (e.g. worldnews).
---

## How to Run Locally

### Prerequisites
1. Python 3.9
2. Install dependencies with 'pip install -r requirements.txt'

### Steps
1. Clone the repository:
  git clone https://github.com/31i731/...
  cd ...
2. Run the notebook:
  jupyter notebook sentiment_analyzer.ipynb
3. (Optional) Update the dataset by running the scraping script.


## Next Steps

  - Fine-tune a Hugging Face model on this dataset to improve sentiment classification accuracy.
  - Extend the analysis to include other subreddits for broader insights.
