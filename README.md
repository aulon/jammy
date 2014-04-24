jammy
=====

A musical accompaniment system, trained using Echo State Networks to listen to a leading track (default: guitar) and play along by generating an accompanying track (default: bass). The code is not yet in a solid state (only minor error checking), and it is what I am using for my Bachelor Thesis.



<b> Prerequisites </b>:
Besides matlab, the tools <a href='http://www.fourmilab.ch/webtools/midicsv/'>midicsv and csvmidi</a> are needed to convert between midi and csv files. The script expects csv files created by midicsv.

<b> Main Scripts </b>: 

music.m : To train the network (file names are hard-coded) All training and testing data should be in 1 file.
run.m : To run the network. In the top rows it is determined which portion of the data will be used as testing data.

<b> Limitations </b>: 
1. So far the network parameters are not fully optimized, I am still playing around with those.
2. For each of the 2 instruments the system currently supports only 1 voice (1 line of melody). This also means that chords are not yet supported. Whenever chords appear in the train/test data, only the top note is selected.

<b> File structure </b>: 
/music/ : main scripts
/music/csv/ : This is where I currently keep all the csv files.
/music/midi/ : all.mid is the training data. all other files are results of tests I have done so far.