# Resume-Parser

This code is an implementation of a pipeline that pulls experience and talents from resume texts and groups them into several domains or categories, such as data science, web development, etc. There are various steps in the pipeline, which are described below:

1)	The required libraries, including os, re, pandas, numpy, spacy, and numerous classes and functions from scikit-learn, are first imported.

2)	The 'en_core_web_sm' package is used to load the English Spacy model into memory.

3)	The 'extract_skills' function is defined. It accepts a resume text as input, parses it using Spacy, and then utilises the Matcher class to extract skills. A list of the extracted skills is then returned by the function.

4)	The function "extract_experience" is defined. It takes a resume text as input, parses it using Spacy, and pulls out experience information by searching for words like "experience," "work," "position," and "employment." The retrieved experience data is then returned by the function.

5)	The 'preprocess_resume' function is described. It accepts a resume text as input, parses it using Spacy, and then preprocesses it by removing all but the pertinent words—such as nouns, adjectives, and verbs—that are likely to provide information about a candidate's abilities and experience. The preprocessed text is then returned by the function.

6)	The 'preprocess_resume' function is used to preprocess the resume dataset after it has been loaded from a CSV file.

7)	For each resume in the dataset, the 'extract_skills' and 'extract_experience' functions are used to extract the relevant data.

8)	There are training and testing sets created from the dataset.

9)	The Pipeline class of scikit-learn is used to define a text categorization model. CountVectorizer, TfidfTransformer, and MultinomialNB are the three components of the model. The text input is transformed into a matrix of token counts in the CountVectorizer phase, normalised in the TfidfTransformer step, and then classified into different domains or categories using the Naive Bayes algorithm in the MultinomialNB step.

10)	The 'fit' approach is used to train the text classification model on the training set of data.

11)	The 'predict' method of the text classification model is used to forecast the domain of each resume in the testing set.

12)	The classification report is printed, displaying each domain's precision, recall, and F1 score.

13)	Using the CountVectorizer class from scikit-learn, the skills and experience columns from the training and testing sets are converted into matrices of token counts.

14)	The 'hstack' method of numpy is used to combine the two matrices into a single matrix.

15)	Scikit-Learn's Pipeline class is used to create a model for classifying abilities and expertise. There is only one step in the model: MultinomialNB.

16)	The combined matrix of token counts is used to train the skills and experience categorization model using the 'fit' method.

17)	The 'predict' method of the skills and experience categorization model predicts the domain of each resume in the testing set.

18)	The classification report is printed, displaying each domain's precision, recall, and F1 score.

19)	Imported is the PyPDF2 library, which is used to extract text from PDF documents.

20)	A PyPDF2 reader object is created after a PDF file is opened in binary mode.

21)	The 'extract_text' method of the PyPDF2 reader object is used to determine how many pages are in the PDF file and to extract the text from each page.

22)	The text that was extracted is printed.

23)	The learned models are used to predict the fresh resume's domain.
