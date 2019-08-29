# Basic_Machine_Learning

This is a simple neural network using Keras for the HZZ off-shell analysis
This work is based on the following tutorails:
https://github.com/YaleATLAS/CERNDeepLearningTutorial/blob/master/data_handling.ipynb
https://github.com/YaleATLAS/CERNDeepLearningTutorial/blob/master/deeplearning_intro.ipynb

There is a conversion code file that converts the root files to h5 files that can be used when working with Pandas Dataframes. 

Here we are trying to differentiate between a signal and backgound. We are looking at ggF signal, ggZZ background and qqZZ background in the off-shell region (m4l between 220 and 2000 GeV).
There is significant destructive interference between the ggHZZ singal and ggZZ backgound in this region; we have Full process (SBI) =  Singal (S) + Background (B) + Interference (I).

Here we are using the neural netwrok to differentiate the Higgs only sample against ggZZ bkg and qqZZ background although we also have a significant number of signal events in the interference.

The variables used in the inputs to the NN are as follows:

a. Madgraph ME : These are calculated using the MadGraph Matrix element calculator.

ME ggZZ higgs

ME ggZZ box

ME ggZZ full

ME QCD qqZZ

b. Spin variables: as defined in arXiv:1001.3396.

cos theta*

Phi1

cos theta1

Phi

c. energy variables

mZ1

mZ2

pT4l

