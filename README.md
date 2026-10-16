# Learning Natural Language Processing

A collection of Jupyter notebooks covering text preprocessing and feature representations with NLTK, scikit-learn, and Gensim.

## Topics and notebooks

| Notebook | Focus |
| --- | --- |
| `Stemming.ipynb` | Sentence and word tokenization examples |
| `Text Preprocessing-Stopwords With NLTK.ipynb` | Stopword removal, Porter/Snowball stemming, and lemmatization |
| `Lemmatization.ipynb` | WordNet lemmatization with part-of-speech choices |
| `Parts_of_speech_tagging.ipynb` | Tokenization and POS tagging |
| `Named_Entity_Recognition.ipynb` | Named-entity chunking and a tree display |
| `BagOfWordsPractical.ipynb` | Binary bag-of-words and n-gram features |
| `TF-IDFPractical.ipynb` | TF-IDF and bigram representations |
| `Word2Vec_practical.ipynb` | Pretrained word vectors, similarity, and nearest words |

`SMSSpamCollection.txt` supplies tab-separated SMS labels and messages for the feature-extraction examples. `Tokenisation_Example.ipynb` currently has no executable example.

## Run locally

Use Python 3 in a virtual environment:

```bash
git clone https://github.com/Sanskar1314/Learning_NLP.git
cd Learning_NLP
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab numpy pandas nltk scikit-learn gensim
jupyter lab
```

On Windows, activate with `.venv\Scripts\activate`. Launch Jupyter from the repository root and run the notebook cells in order.

## Language resources

Download the resources used by the examples in a notebook cell:

```python
import nltk
for resource in [
    "punkt", "punkt_tab", "stopwords", "wordnet",
    "averaged_perceptron_tagger_eng", "maxent_ne_chunker",
    "maxent_ne_chunker_tab", "words",
]:
    nltk.download(resource)
```

The Word2Vec notebook downloads `word2vec-google-news-300` through Gensim; this requires internet access, disk space, and substantial memory. Named-entity tree rendering with `.draw()` requires a local GUI with Tk support. These are independent learning exercises rather than a single application.
