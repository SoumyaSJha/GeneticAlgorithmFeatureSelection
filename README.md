# Genetic Algorithm for Feature Selection in Text Categorization

## Project Overview
Text categorization is the process of as-
signing text documents to predefined categories. It is
a challenging task, especially when dealing with large
volumes of unstructured text. One of the main challenges
is feature selection. Features are the distinguishing char-
acteristics of a text document, such as words, phrases,
or topic-specific keywords. In large datasets, the number
of features can be overwhelming, leading to the risk of
overfitting.
To address this challenge, we propose a Genetic
Algorithm based feature selection technique that uses
a probabilistic feature selection approach. Unlike usual
implementations of genetic algorithm-based feature se-
lection, our proposed method implements it as a fil-
ter method rather than a wrapper method, enhancing
computational efficiency without compromising accuracy.
We also implement a chi-square-based feature selection
technique to compare our results with it.
To test our feature selection techniques, we use
Multinomial Naive Bayes (MNB), Gaussian Naive Bayes
(GNB), and Support Vector Machine (SVM) to do the
binary classification task of categorizing news documents.


## Dataset Used
The dataset employed in this study consists of 200
datapoints, encompassing sports and sci-tech news
articles, making it suitable for binary text classifica-
tion. The dataset is curated to represent a balanced
distribution of articles from both domains, ensuring a
comprehensive evaluation of the classification model.
Each datapoint includes relevant textual content and
corresponding labels indicating whether the article
falls under the sports or sci-tech category. This curated
dataset serves as the foundation for training and eval-
uating the text classification model in the subsequent
sections.

## Discussion
### GA as a Filter Method
Employing GA as a filter method, rather than a
wrapper method, decreases computational complexity
as it avoids the need for repetitive model training. In
our GA approach, dependence on model-specific met-
rics is eliminated, replaced by an evaluation through
a Bayesian framework-based fitness function. This
independence makes it adaptable to various models
and less constrained by model-specific requirements.

### GA before text-extraction
When applying GA directly on text data, you retain
the richness and complexity of the original text. Each
word and its arrangement contribute to the genetic
makeup of individuals in the population. This approach
preserves valuable information, capturing the intrica-
cies and nuances of language that might be lost in
feature extraction.
GA applied on raw text data allows the algorithm to
freely evolve and explore combinations of words and
phrases without predefined features.
GA applied on raw text allows the algorithm to
evolve and discover domain-specific terms or lexicons
that are crucial for the classification task. This can be
especially valuable in domains with evolving language
or specific jargon.

### Probablistic and Bayesian framework based Fitness Function
The fitness function evaluates the occurrence of
words within an individual in relation to two sets
of labels. This approach to evaluating an individual’s
fitness based on word occurrences within predefined
label sets aligns conceptually with the principles of
conditional probability and Bayesian inference. It uti-
lizes prior knowledge (associated words with labels)
and observed data (word occurrences in the individual)
to quantify the likelihood of the individual’s align-
ment with these labels, reflecting a Bayesian approach
to updating beliefs through evidence. The function’s
foundation in conditional probability enables a fine-
grained assessment of word relevance within class, contexts, pinpointing words that uniquely define par-
ticular classes. By integrating a Bayesian framework,
it achieves adaptability. This approach ensures an
information-rich evaluation that captures the intricate
relationships between words and class distinctions.
