# Encoding Categorical Data

As we know, most of Machine Learning algorithms need as input numerical data. We refer as categorical data to those that 
aren't numerical and are strings representing a value, category, or classification. In order to feed the ML algorithms we
need to transform them numbers. For doing so, there are different approaches we may take.

Selecting the encoding is not trivial. It will depend on the nature of the feature.
Some resources about it:

https://machinelearningmastery.com/how-to-prepare-categorical-data-for-deep-learning-in-python/

https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/

https://machinelearningmastery.com/feature-selection-with-categorical-data/

There are three ways for encoding the data:
* Integer Encoding: Where each unique label is mapped to an integer.
* One Hot Encoding: Where each label is mapped to a binary vector.
* Learned Embedding: Where a distributed representation of the categories is learned.