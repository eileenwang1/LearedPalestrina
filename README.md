# Learned Palestrina
This project uses a LSTM model trained on the music of Palestrina to generate music.

## Files
* Generate0.ipynb: a Jupyter notebook that loads weights from trained model to generate music (midi output)
* Training0.ipynb: train the LSTM model from the music of Palestrina
* example_output.mid: example midi output
* data/notes_given: a binary file that stores the music vocabulary of data input
* DataX:
  * Model_Weights: weights for LSTM model every 10 epoch of training
  * training_log.csv: a csv file that stores cross entropy loss and accuracy at every epoch of training
  * char_to_index.json: json file for note-index mapping
* midi_songs: If you want to train your own model, the midi files that are used to train the model should go under this folder. I upload a few midi files as placeholders here.
* scrap_midi.py: the python code for gathering midi files from *ChoralWiki.*
  
## Prerequisites
* python 3
* keras
* music21

## Getting started
* Play example_output.mid to hear an example of the result.<br>
* Run Generate0.ipynb and generate music on your own! The output will be in test_output.mid, and can also be played in Generate0.ipynb
* Run Training0.ipynb to train the model on your own. Note: you will need to put enough midi data under the folder midi_songs. Pay attention to file paths and names when storing and loading data.

## References
1. [Data source] "Giovanni Pierluigi da Palestrina" *ChoralWiki.* 
    <br>http://www1.cpdl.org/wiki/index.php/Giovanni_Pierluigi_da_Palestrina <br>
2. [LSTM model] Gaurav Sharma. "Music Generation Using Deep Learning." *Medium.*
    <br>https://medium.com/datadriveninvestor/music-generation-using-deep-learning-85010fb982e2?<br>
3. [Data processing] Sigurður Skúli. "How to Generate Music using a LSTM Neural Network in Keras" *Medium.*
    <br>https://towardsdatascience.com/how-to-generate-music-using-a-lstm-neural-network-in-keras-68786834d4c5<br>
4. [WebScraper] Samridha Shretha. *Github.*
    <br>https://github.com/SamSamhuns/musical_python/blob/master/scrap_midi/scrap_freemidi_org.py<br>
