---
layout: default
title:  Final Report
---

## Status Video
------------------


## Project Summary
------------------
The purpose of this project is to create a model that, given music as training data, can recreate music of the same genre given a musical start (around 10 notes). The type of music generated will depend largely on the type of music trained on. For example a model trained on Bach will yield Bach-esque results, while other models might have different characteristics. Once this music is generated, we then use Malmo to create a series of note blocks that the agent can play in order to play the music on the Minecraft platform. With the final result of this project, our model can recreate music that is similar to the trained music, with a fair degree of musicality.
<br><br>
A baseline that we seeked to improve on was simply picking notes at random in order to recreate music. Since such a model would have no sense of what might make sense with a given context, a ML component was necessary in order to adapt the model to the pleasing combinations of notes. By doing so, our model was better able to anticipate which notes would be logical to play next, drawing inspiration entirely from the previous notes that it has seen.

## Approaches
-------------

### Baselines
-------------
In the beginning of the project, we used a model that selects notes in a completely random manner, from any possible note. However, we realized that this was not a very fair comparison, as there was a huge disparity in the notes being selected, and there was no reasonable way for the notes to sound musical. Thus since we start the song with the first ten notes of the original song, we only selected random notes out of the pool of notes that we already saw in that ten-note intro. By doing this, we saw a slight improvement in the baseline, though it still sounded far worse than our own finalized model, which is good.

### Random Forest
-----------------

### Recurrent Neural Network
----------------------------

### SVM and other models
------------------------

## Evaluation
-------------

## References
-----------------
- [Music21](https://web.mit.edu/music21/) : Python library to facillitate note and midi parsing
- [Malmo XML Documentation](https://microsoft.github.io/malmo/0.30.0/Schemas/Types.html) : helpful for learning about the formatting of XML mission strings
- [scikit learn](https://scikit-learn.org/stable/) : Python library to handle much of the ML components
- [Karpathy article about RNNs](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) : article describing the effectiveness of RNNs on a variety of applications
