# **Sentiment Analysis and Classification of Ruangguru's Clash of Champions YouTube Comments**

This project performs sentiment analysis and builds a text classification model to categorize YouTube comments from Ruangguru Clash of Champions. We use sentiment analysis to initially label our unlabeled dataset, classifying comments as negative, neutral, or positive. The goal is to create a model that can accurately label new comments, potentially expanding beyond sentiment to categorize them based on topic, relevance, or engagement. This model could benefit Ruangguru by automating comment analysis and improving community engagement.

**Key points:**

* **Dataset:** YouTube comments from Ruangguru Clash of Champions episodes 1-3.
* **Labeling:** Initial labeling using sentiment analysis.
* **Model:** Text classification model trained on sentiment-labeled comments.
* **Potential:** Expand model beyond sentiment, benefit Ruangguru through automated comment analysis.

**Credit:**

1. Ruangguru YouTube
2. normalized_term from [teguhary's GitHub](https://github.com/teguhary)
3. MPStemmer() from [ariaghora's GitHub](https://github.com/ariaghora)
4. Lexicon for sentiment analysis from [angelmetanosaa's GitHub](https://github.com/angelmetanosaa)

**Q&A:**

1.
- **Q:** Why not create different models for each episode?
- **A:** Creating separate models for each episode would result in insufficient training data for each individual model, leading to poorer performance. Combining the data allows for a more robust model.
2.
- **Q:** Why use `normalized_term` from [teguhary's GitHub](https://github.com/teguhary)??
- **A:** Teguhary's `normalized_term` function is chosen for its comprehensive normalization capabilities, exceeding other available options in my experience.
3.
- **Q:** Why use `MPStemmer()` instead of Sastrawi?
- **A:** Please refer to [ariaghora's GitHub](https://github.com/ariaghora) for a detailed comparison of `MPStemmer()` and Sastrawi, outlining the reasons for choosing `MPStemmer()` in this project.
4.
- **Q:** Why use the Lexicon for sentiment analysis from [angelmetanosaa's GitHub](https://github.com/angelmetanosaa)?
- **A:** While not finding a superior alternative, this lexicon, taught by Dicoding Academy, was a readily available and suitable option for the sentiment analysis task.
5.
- **Q:** Could any potential problems arise from using [angelmetanosaa's GitHub](https://github.com/angelmetanosaa) lexicon for inference ?
- **A:** Yes, there could be problems. The lexicon used in the model has an imbalanced distribution, with 3609 positive terms and 6607 negative terms. This imbalance could lead to an overestimation of negative sentiment when analyzing comments. However, if you don't have alternative options readily available, using this lexicon might still provide some valuable insights despite its limitations.
6.
- **Q:** Are there any potential issues to be aware of with this project?
- **A:** Yes, as this project involves text classification in Bahasa Indonesia, there are limitations in the resources available. Specifically, the tools for normalization, stemming, and lexicon building are not as robust as those available for English. This could impact the accuracy and effectiveness of the analysis.

# **[Project's Repository Link](https://github.com/kevinadityaikhsan/ruangguru-sentiment-analysis-classification)**
