# Character_Model
# Overview -
This project tests to see if an LSTM neural net can continue a passage of text using character prediction.
The code is split into 2 sections, a training/testing loop and then a sampling
section that takes an unseen passage of 20 characters and uses beam search to
create multiple potential completions of 100 characters.
I used a softmax temperature to trade off quality with the diversity of the samples.

I ran the epochs until the test loss was no longer decreasing,
as this indicates that the neural net is now overfitting to the data.

# Results -
The neural net successfully trained for around 50 epochs.
The samples went from being completely random to being able to produce a string
of correctly spelt words with mainly correct grammar.
However it was not able to produce passages of profound meaning.
Here are some examples:

Sample text: y country good. KING HENRY. In any case be not too rough in terms,
             For he is fierce and cannot brook

Given text: y country good. KING

Generated text: y country good. KING RICHARD. Thou shall be now, and make him
                indeed of your son, and that I stand a

This demonstrates that while all the words are real and the grammar just about
works, it is meaningless text. It also has a bias towards more common words,
explaining the lack of meaning.
