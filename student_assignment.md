# Master Student Assignment

## Speaker gender classification
### Instructions
* Please find and download part of the LibriSpeech [here](http://www.openslr.org/12/). Find some time to read the documentation of the database. Download the dev-clean corpus, which is relative small in size. This database contains directories with ids. Each id represents one speaker and contains audio files associated with that speaker. You will also find a file that indicates the gender of each speaker.
* In case you have computational issues, please feel free to select a subset of the dataset. However, try to keep at least 18 speakers (9 male and 9 female).
The next step would be to extract features for the audio files. The most common type of features are the MFCC features. Feel free to use existing libraries in order to extract MFCC features for all the audio files of your dataset.
* Once you have the MFCC features extracted, you can start playing with various Machine Learning Algorithms. We would like you to perform a gender classification task. For each audio file you create a gender label. Build train and test (unseen while training) sets. Train a classifier on the train set and predict the labels of the test set. Measure accuracy and report performance. Try to experiment with at least 4 classifiers. Use two of them as baselines (one naive and one more sophisticated), a neural network and a deep learning model, such as a CNN. Once again, feel free to use any libraries that are convenient for you.
* For the aforementioned tasks, analyse and interpret the results. Don’t focus only on numbers. Try to explain why an algorithm performs better/worse than the others. The important part for us is to see the way you think and deal with a project like that. Don’t be afraid of interpreting the results and making mistakes. We are not going to judge that negatively.

### Deliverables

* It would be great to use Jupyter Notebook for this assignment. Please try to show us your coding skills. Clean code with comments and correct programming principles are much appreciated.
* The assignments should be pushed on GitHub. Please share the link of the repository with us when you are done with the assignment

### Timeline
You have two weeks to complete the assignment. In case you have any questions or would like to discuss the assignment before you start, please feel free send me an email.