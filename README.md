# **Sentiment Analysis and Classification of Ruangguru's Clash of Champions YouTube Comments**

This project performs sentiment analysis and builds a text classification model to categorize YouTube comments from Ruangguru Clash of Champions. We use sentiment analysis to initially label our unlabeled dataset, classifying comments as negative, neutral, or positive. The goal is to create a model that can accurately label new comments, potentially expanding beyond sentiment to categorize them based on topic, relevance, or engagement. This model could benefit Ruangguru by automating comment analysis and improving community engagement.

**Key points:**

* **Dataset:**
  - YouTube comments extracted from Ruangguru's Clash of Champions episodes 1-3.
  - Date of Collection: Tueday July 29, 2024 (9:26 AM)
  - Tool: youtube_comment_downloader from [egbertbouman's GitHub](https://github.com/egbertbouman)
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
- **A:** While not finding a superior alternative, this lexicon, taught by [Dicoding Academy](https://www.dicoding.com/), was a readily available and suitable option for the sentiment analysis task.
5.
- **Q:** Could any potential problems arise from using [angelmetanosaa's GitHub](https://github.com/angelmetanosaa) lexicon for inference ?
- **A:** Yes, there could be problems. The lexicon used in the model has an imbalanced distribution, with 3609 positive terms and 6607 negative terms. This imbalance could lead to an overestimation of negative sentiment when analyzing comments. However, if you don't have alternative options readily available, using this lexicon might still provide some valuable insights despite its limitations.
6.
- **Q:** Are there any potential issues to be aware of with this project?
- **A:** Yes, as this project involves text classification in Bahasa Indonesia, there are limitations in the resources available. Specifically, the tools for normalization, stemming, and lexicon building are not as robust as those available for English. This could impact the accuracy and effectiveness of the analysis.

## **Results**

1. **TF-IDF with Multi-Layer Perceptron** ranked second, achieving an accuracy of 92.7%. This model required only 12 minutes for training, faster than the other models.

2. **TF-IDF with Dense Layer** ranked third, with a test accuracy of 92.6%. This model showed the highest risk of overfitting, evidenced by a 4.5% difference between training (97.1%) and test accuracy. Training took 32 minutes across 25 epochs, with each epoch averaging 77 seconds.  The model demonstrated low variance, as shown by the consistent loss and accuracy plots.

3. **Word Embedding with Global Average Pooling Layer** ranked last, with an accuracy of 90.3%. This model exhibited a lower risk of overfitting than the previous model (TF-IDF with Dense Layer), with a 1.2% difference between training (89.1%) and test accuracy. Training took 16 minutes across 29 epochs, with each epoch averaging 33 seconds. The model showed high variance, indicated by fluctuations in the loss and accuracy plots.

4. **Word Embedding with Global Average Pooling Layer and Dense Layer** achieved the highest accuracy of 93.8%. This model demonstrated the lowest risk of overfitting among all models, with a 0.2% difference between training (93.6%) and test accuracy. Training took 31 minutes across 52 epochs, with each epoch averaging 36 seconds. The model showed high variance, indicated by fluctuations in the loss and accuracy plots.

## **Conclusion**

Based on the results, the **Word Embedding with Global Average Pooling Layer and Dense Layer** model is recommended for the following reasons:

* **Highest Accuracy:** It achieves the highest accuracy of 93.8%.
* **Lowest Risk of Overfitting:** It demonstrates the lowest risk of overfitting among all models, with only a 0.2% difference between training and test accuracy.

While the model does exhibit high variance, this could potentially be addressed through techniques like regularization or using more training data.

This project successfully developed a text classification model for categorizing YouTube comments from Ruangguru's Clash of Champions episodes. The model demonstrates the potential for automated comment analysis and sentiment identification, which can be a valuable tool for Ruangguru to understand and engage with its audience. While the model has achieved promising results, there are areas for improvement and considerations for future applications.

## **Recommendations**

1. **Address Class Imbalance:** The imbalanced lexicon used for sentiment analysis may lead to biased results, with a tendency to overestimate negative sentiment. Efforts should be made to balance the lexicon or explore alternative sentiment analysis techniques.

2. **Enhance Preprocessing:** The effectiveness of text preprocessing can be further enhanced. Consider incorporating advanced techniques like spell checking, slang handling, and negation handling to improve the accuracy of feature extraction and model performance.

3. **Explore Deep Learning Models:** The project currently utilizes machine learning models. Exploring deep learning architectures, such as recurrent neural networks (RNNs) or transformers, could potentially enhance the model's ability to capture contextual nuances in comments.

4. **Expand Labeling Categories:** Consider expanding the labeling categories beyond sentiment. Incorporating categories like topic, relevance, or engagement level can provide Ruangguru with more comprehensive insights into their audience's feedback and preferences.

5. **Continuous Model Improvement:** As new data becomes available, the model should be continuously retrained and updated to maintain its accuracy and adapt to evolving language patterns and trends in the comments.

By implementing these recommendations, Ruangguru can further refine its comment analysis capabilities, gain deeper insights into audience sentiment and engagement, and leverage this information to enhance its content and community interaction strategies.
