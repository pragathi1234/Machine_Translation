# Machine Translation

##### What is Machine Translation?

- Machine Translation is the task of automatically converting one natural language into another, preserving the meaning of the input text, and producing fluent text in the output language.

    There are four types of machine translation:
        - Statistical Machine Translation or SMT.
        - Rule-based Machine Translation or RBMT.
        - Hybrid Machine Translation or HMT.
        - Neural Machine Translation or NMT.

    In this project we have implemented Neural Machine Translation using Bahdanu Attention mechanism to translate the     English text to Telugu.

##### What is NMT?

- Neural machine translation, NMT for short, is the use of neural network models to learn a statistical model for machine translation.

- The key benefit to the approach is that a single system can be trained directly on source and target text, no longer requiring the pipeline of specialized systems used in statistical machine learning.

#### Area of Application NMT dealing with:
- According to the graphic below, Google Translate delivers translations from Spanish, Chinese, and French to English and vice versa with different levels of accuracy on scale with human translators.


<img src="https://github.com/pragathi1234/Machine_Translation/blob/main/images/google_analysis.png?raw=true:, width=100" alt="My Image" width=500>

A graphic from Google Research highlighting the 2016 accuracy levels of Google Translate

- Machine translation solutions are progressively being used in more areas of business, providing new applications and improved machine-learning models, as their accuracy levels rise.
- Numerous applications evolved which where using translators now-a-days, by integrating our model to any kind of application that serves end users to understand the english text to telugu.
- Applications involves:
    - Agriculture.
    - Healthcare.
    - Finance.
    - Software and Technology.
    - Ecommerce.


#### About Data:
- We have used two datasets for modeling, data files are collected from Google Translate API and [manythings](http://www.manythings.org/anki/)
    - The Google Translate API data consist of 2 columns and 5615 rows
    - [Manythings](http://www.manythings.org/anki/) data consist of 2 columns and 88370 rows.
    - Shape of final data is (93985 X 2).
    
#### Tasks Performed.
- Loading the text file which contains two columns with English as source and Telugu as target.
- Preprocessing the data until it is good fit for modeling.
- Performed Tokenization to break the raw text into small chunks.
- Split the data into train test for modeling and evaluation.
- Modeling:
    - Implemented Encoder-Decoder with Attention.
    - Applied Predefined Hugging Face Models:
        - facebook/mbart-large-50-one-to-many-mmt.
        - Helsinki-NLP/opus-mt-en-dra.
        - Helsinki-NLP/opus-mt-en-mul.
- Evaluated all the models and compared the output with the Google translate API and retrieved the BLEU score for each model.

### Results
![output](https://github.com/pragathi1234/Machine_Translation/blob/main/images/Screen%20Shot%202022-05-06%20at%202.49.39%20AM.png)

### Conclusion:
In this project, we propose different mechanisms for Neural Machine Translation: the global approach that looks at all source positions at all times, and a predefined model. When compared to the Helsinki-NLP/opus-mt-en-dra and facebook/mbart-large-50-one-to-many-mmt models, Helsinki-NLP/opus-mt-en-mul, predefined models outperformed this task. We put our models to the test in NMT translation tasks between English to Telugu.

### Future Developments
- OpenAPI GPT is the most powerful Transformer to perform language translation. Because of the potential for misuse, the developers have refused to open source the entire model.
- Starting from the very bottom of a deep neural network, BERT represents "bank" using both its previous and next contexts — "I accessed the... account" — making it deeply bidirectional. BERT will also be the most trending technique for Machine Translation.

### References:

- https://www.tensorflow.org/text/tutorials/nmt_with_attention
- https://arxiv.org/pdf/1508.04025.pdf
- https://towardsdatascience.com/neural-machine-translation-nmt-with-attention-mechanism-5e59b57bd2ac
- https://emerj.com/ai-sector-overviews/machine-translation-14-current-applications-and-services/
- https://arxiv.org/pdf/1706.03762.pdf
- https://arxiv.org/pdf/1409.0473.pdf
