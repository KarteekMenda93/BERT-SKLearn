# BERT-SKLearn

Under the hood, the model is actually made up of two models.

BERT processes the sentence and passes along some information it extracted from it on to the next model.
The next model, a basic Logistic Regression model from scikit learn will take in the result of DistilBERT’s processing, and classify the sentence as either positive or negative (1 or 0, respectively).
The data we pass between the two models is a vector of size 768. We can think of this of vector as an embedding for the sentence that we can use for classification.
