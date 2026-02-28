# DETECT "isn't it"
I was listening to some lectures on youtube, and I found something beautiful which is a person using the word `isn't it`. I collected audio transcripts from 15 lectures and `isn't it` was used around **543 times**. I felt that's crazy and I wanted to build a ML/DL model which tells me when will the tutor says `isn't it`.

## Problem Approach
- It was a binary classification problem, either the next word will be `isn't it` or not.
- I had to preprocess the data
  - Conversion to lower case and splitting them to words
  - Creating NGrams (grouping words together, I grouped 8 words together. So, first 6 words are input and the last 2 words are for output)
  - Example: (is', 'first', 'guess', 'is', 'x', 'not', "isn't", 'it') in this the first 6 words are input and this is a positive example where `isn't it` will occur
  - I created a dataset which is in "data/processed_data.csv"
- Then I simply created an LSTM without dropout and early stopping and it worked :)
