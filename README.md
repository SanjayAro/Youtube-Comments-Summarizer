# YouTube Comments Summarizer

The YouTube Comments Summarizer is a Python-based tool that allows you to collect and analyze comments on YouTube videos.
Using the YouTube API and the Zero-shot classification method, the tool 
can classify comments into four categories: positive feedback, negative feedback, requests for future videos, and doubts on the video.

## Table of Contents

- [Extracting comments using the YouTube API](#extracting-comments-using-the-youtube-api)
- [Zero-shot classification](#zero-shot-classification)
- [Summarization Techniques](#summarization-techniques)
  - [Extractive Summarization](#extractive-summarization)
  - [Abstractive Summarization](#abstractive-summarization)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Extracting comments using the YouTube API

To extract comments using the YouTube API, you will need to create a Google Cloud Platform project and enable the YouTube Data API v3. Then, you can use the `Comments` endpoint to retrieve comments for a specific video.


## Zero-shot classification

Zero-shot classification is a machine learning technique that allows you to classify text into multiple categories without having to train a specific model for each category. Instead, the technique relies on a pre-trained language model that can generate representations for any input text, and a set of category labels that are used as prompts for the model. The language model then generates a score for each label, indicating the likelihood that the input text belongs to that category.

In the YouTube Comments Summarizer, we use the Hugging Face's `zero-shot` classifier to classify comments into four categories: positive feedback, negative feedback, requests for future videos, and doubts on the video. The classifier is pre-trained on a large corpus of text and can generate accurate classification results without requiring training on specific datasets.

## Summarization Techniques

The YouTube Comments Summarizer uses two different summarization techniques to summarize the classified comments: extractive summarization and abstractive summarization.

### Extractive Summarization

Extractive summarization is a text summarization technique that involves selecting a subset of sentences from the input text to form a summary. The selected sentences are typically those that contain the most important information or convey the key ideas of the text.

In the YouTube Comments Summarizer, we use the Gensim library's `summarize` function to perform extractive summarization of the classified comments. The `summarize` function uses a variation of the TextRank algorithm to identify the most important sentences in the input text and return them as a summary.

### Abstractive Summarization

Abstractive summarization is a text summarization technique that involves generating a summary that is not necessarily present in the input text. Instead, the technique involves generating new text that conveys the key ideas of the input text in a more concise

## Usage

The YouTube Comments Summarizer script can be used to analyze comments on any YouTube video. Simply provide the video ID and the number of comments to retrieve, and the tool will collect and classify the comments into four categories: positive feedback, negative feedback, requests for future videos, and doubts on the video.


## Contributing

Contributions to the YouTube Comments Summarizer project are welcome! If you find any issues or have any suggestions, feel free to create an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
