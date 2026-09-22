# News Article Summarizer

## Overview

News Article Summarizer is a Natural Language Processing (NLP) project that automatically generates a concise summary from a given news article.

The project uses a pre-trained Transformer model from Hugging Face to perform abstractive text summarization.

The user provides a news article as input, and the model generates a shorter summary containing the main information from the article.

## Technologies Used

* Python
* Natural Language Processing (NLP)
* Hugging Face Transformers
* PyTorch
* SentencePiece
* Jupyter Notebook

## Model Used

The project uses the following pre-trained Transformer model:

`sshleifer/distilbart-cnn-12-6`

The model is designed for text summarization and is used to generate summaries from news articles.

## How It Works

The project follows these steps:

1. The user provides a news article.
2. The article is passed to the summarization pipeline.
3. The Transformer model processes the input text.
4. The model generates a concise summary.
5. The generated summary is displayed to the user.
6. The project can also calculate the reduction in the number of words between the original article and the generated summary.

## Project Structure

```text
news-article-summarizer/
│
├── news_article_summarizer.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the Project Directory

```bash
cd news-article-summarizer
```

### 3. Install the Required Packages

```bash
pip install -r requirements.txt
```

## Requirements

The project uses the following main Python packages:

* `transformers==4.57.1`
* `torch==2.14.0`
* `sentencepiece==0.2.2`

The complete package versions are available in `requirements.txt`.

## Usage

### 1. Start Jupyter Notebook

Run:

```bash
jupyter notebook
```

### 2. Open the Notebook

Open:

```text
news_article_summarizer.ipynb
```

### 3. Run the Notebook

Run the notebook cells from top to bottom.

The summarization model will be loaded automatically.

### 4. Enter a News Article

The project allows the user to enter a news article and generate a summary.

Example:

```text
Enter your news article:
[Enter your article here]
```

The generated summary will then be displayed.

## Example

### Input

A news article containing information about a scientific discovery.

### Output

The Transformer model generates a shorter summary containing the main information from the article.

## Text Reduction

The project also compares the number of words in the original article with the number of words in the generated summary.

For example:

```text
Original words: 93
Summary words: 29
Text reduction: 68.82%
```

The percentage represents the reduction in word count between the original article and the generated summary.

## Key Concepts Demonstrated

* Natural Language Processing
* Text summarization
* Abstractive summarization
* Transformer models
* Pre-trained models
* Hugging Face Transformers
* PyTorch
* Model inference
* Text processing
* Jupyter Notebook

## Functionality

The main summarization functionality is implemented using a Python function:

```python
def summarize_article(text):
    result = summarizer(
        text,
        max_length=60,
        min_length=15,
        do_sample=False
    )

    return result[0]["summary_text"]
```

This function accepts an article as input and returns the generated summary.

## Limitations

* The model runs on CPU in the current setup, so inference may take some time.
* The project currently uses a pre-trained summarization model without additional fine-tuning.
* Very long articles may require additional text-processing or chunking.
* Generated summaries may not always contain every important detail from the original article.

## Future Improvements

* Add a web interface using Streamlit or Django.
* Support longer news articles using text chunking.
* Add multiple summarization models.
* Add summary quality evaluation.
* Add a graphical user interface.
* Deploy the application as a web service.
* Add support for summarizing news articles from URLs.

## Learning Outcomes

Through this project, the following concepts are demonstrated:

* Understanding of NLP applications.
* Working with pre-trained Transformer models.
* Using Hugging Face Transformers pipelines.
* Performing abstractive text summarization.
* Loading and using a pre-trained deep learning model.
* Creating reusable Python functions.
* Measuring text reduction.
* Working with Jupyter Notebook and Python environments.

## Author

**Sowjanya Kodi**

B.Tech – Computer Science and Engineering

---

## License

This project is created for learning and portfolio purposes.
