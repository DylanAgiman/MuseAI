---
layout: default
title: Status
---

## Project Summary
------------------

## Approach
-----------

## Evaluation
-------------

## Remaining Goals and Challenges
---------------------------------
To reach this status report milestone, we focused more on much of the logistics of integrating the music into Minecraft and Malmo, and less on refining the machine learning algorithms. Our current project is limited because it lacks a lot of the refinement that comes with optimizing the ML components of the project. For example, the project currently only trains on the soprano parts of songs, whereas the actual song might have 3 or 4 parts that are playing in unison. A logical next step might be to find a way to intelligently train on the other parts of the song while still maintaining a coherence with the song as a whole.
<br><br>
In addition, as our project currently stands, we use a simplified model for the generating of new music, namely a random forest. This method has its drawbacks, and an RNN might simplify the training or coherence aspects greatly. Thus, the next step might be to shift to a more neural-network oriented model, which has been shown to have better results, especially in the music generation field.
<br><br>
Finally, the evaluation metric that we used for this status report is very simplified, and may not represent the true "musicality" of the generated piece. Currently, to evaluate the success of a generated piece of music, we compare each note individually to the notes of a piece of music which we have not trained on. If the note is identical to the note in the validation piece, then that would count as a "hit", which is equivalent to an accurate note. Otherwise the note would register as a "miss", and is given 0 credit for accuracy. However, this is merely a measure of the success of the model to recreate a piece exactly, whereas we might be more interested in evaluating the overall musicality of a piece. Therefore another future step might be to change the evaluation function such that it rewards notes in the same key, or notes that are similar to the validation notes.

## Resources Used
-----------------
- [Music21](https://web.mit.edu/music21/) : Python library to facillitate note and midi parsing
- [Malmo XML Documentation](https://microsoft.github.io/malmo/0.30.0/Schemas/Types.html) : helpful for learning about the formatting of XML mission strings
- [scikit learn](https://scikit-learn.org/stable/) : Python library to handle much of the ML components
- [Karpathy article about RNNs](http://karpathy.github.io/2015/05/21/rnn-effectiveness/) : article describing the effectiveness of RNNs on a variety of applications
