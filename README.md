# BOOKBYBRAIN
I don't know why does it happen but many a times we start reading a book and then later find no interest in it again.It remains there unopened and turning old day by day!!Why does
it hapen that something we found out to be interesting seems interesting no longer.Our project BookByBrain aims in helping you find the right book aaccording to your mood by using
your brain signals.
# ABSTRACT
Emotion is a complicated physiological response of human beings,
which plays an important role in our daily life and work. Positive emotions help us to improve human health and work efficiency,
while negative emotions may cause health problems. Nowadays
emotion recognition has been widely used in many scientific and
technological fields, such as human-computer interaction, distance
education, and health care, etc., and has gained wide attention of
academic research.

In general, there are two different ways to recognize emotion.
One is to directly consider non-physiological signals such as facial
expressions, speech, body gesture, text to construct
models, which collect data in a non-invasive way. However, for this
approach, it is difficult to obtain correct emotions if people deliberately mask their true feelings.
<img width="687" alt="Screen-Shot-2021-07-28-at-8 18 31-AM" src="https://user-images.githubusercontent.com/83583106/154895385-160359d3-f265-4159-a783-b05eb023fe4a.png">

Another approach is to consider
physiological signals such as heart rate, skin conductivity,
respiration, and EEG to classify emotions. EEG, signaled by the
central nervous system, is a direct response to brain activity and is
more objective and reliable in capturing real human emotions.

![EEG-signals-and-their-corresponding-first-five-IMFs](https://user-images.githubusercontent.com/83583106/154896448-0d651fb0-8d1f-4d8a-af26-4eca9906b34f.png)

The first part of our project aims at classifying the emotions based on the eeg signals using the preprocessed data and apply Deep Learning algorithms. The second part is to
suggest a book based on the mood detected by the algorithm.

![electroencephalogram_eeg](https://user-images.githubusercontent.com/83583106/154898830-7e66f755-e254-4504-ba22-3ba07032a90f.jpg)
# DATASET
We used the SEED-V dataset for our project which can be found on: `https://bcmi.sjtu.edu.cn/home/seed/seed-v.html`.The dataset contained preprocessed and raw files as well. For our
purpose we used the preprocessed dataset.The preprocessed dataset were first downsampled to a 200 Hz sampling rate. To filter the noise and remove the artifacts, the EEG data are then processed with a bandpass filter between 1 Hz and 75 Hz. Afterward, we extract differential entropy (DE) features within each segment at 5 frequency bands: 1) delta: 1-4 Hz; 2) theta: 4-8 Hz; 3) alpha: 8-14 Hz; 4) beta: 14-31 Hz; and 5) gamma: 31-50 Hz.
For the book dataset we used `https://www.kaggle.com/michaelrussell4/10000-books-and-their-genres-standardized` which we found on Kaggle easily.
# MODEL
We tried using a basic 1D ConvNet which gave us a great val accuracy of 0.98%. We also tried using LSTM and RCNN and decided later which worked out the best of all.Next using cosine similarity we predicted which book can be given to the our subject.
