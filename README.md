# MARCUS AURELIUS QUOTE FINDER

Based on what a user is feeling currently, the app will find a quote from Marcus Aurelius that is relevant to the user's current state of mind.
It uses quotes cleaned from https://www.gutenberg.org/files/2680/old/medma10.txt into singular quotes, 
A GoEmotions model to get 27 emotion logits which are used as embeddings and indexed using FAISS.
The prototype is available in a jupyter notebook, while development of the app is underway.

## Technologies
BERT, FAISS, GoEmotions, Pytorch

## Introduction
In times of uncertainty, it is important to have a source of inspiration and motivation.
Marcus Aurelius was a Roman Emperor who wrote a book called Meditations, which is a collection of his thoughts and reflections.
The idea is to showcase how complex emotions between people can be compared using embeddings and FAISS.

## How it works
The app takes in a user's input, which is a sentence describing how they are feeling.
The sentence is then passed through a BERT model to get 27 emotion logits.
The logits are then used as embeddings and indexed using FAISS.
The app then returns a quote from Marcus Aurelius that is relevant to the user's current state of mind.

## NOTE:
The app is still in development, and is not yet available for use.
Please refer to the prototype in the jupyter notebook. 

## Example
`User Text`:

I am so in love today. I have fallen in love with someone

`Quotes (top-2)`:

XXII.  The earth, saith the poet, doth often long after the rain.  So is the glorious sky often as desirous to fall upon the earth,  which argues a mutual kind of love between them.  And so (say I)  doth the world bear a certain affection of love to whatsoever shall come  to pass With thine affections shall mine concur, O world.  The same  (and no other) shall the object of my longing be which is of thine.  Now that the world doth love it is true indeed so is it as commonly said,  and acknowledged ledged, when, according to the Greek phrase,  imitated by the Latins, of things that used to be, we say commonly,  that they love to be. 

XXXV.  Fit and accommodate thyself to that estate and to those occurrences,  which by the destinies have been annexed unto thee; and love  those men whom thy fate it is to live with; but love them truly.  An instrument, a tool, an utensil, whatsoever it be, if it be fit  for the purpose it was made for, it is as it should be though  he perchance that made and fitted it, be out of sight and gone.  But in things natural, that power which hath framed and fitted them,  is and abideth within them still:  for which reason she ought  also the more to be respected, and we are the more obliged (if we  may live and pass our time according to her purpose and intention)  to think that all is well with us, and according to our own minds.  After this manner also, and in this respect it is, that he that is  all in all doth enjoy his happiness. 

## References
[1] Marcus Aurelius Meditations - https://www.gutenberg.org/files/2680/old/medma10.txt, for license see https://www.gutenberg.org/policy/license.html
[2] GoEmotions: A Multilingual Emotion Corpus for Text Classification, https://arxiv.org/abs/2005.00547
[3] Models for inference, or base modeling. https://huggingface.co/monologg/bert-base-cased-goemotions-original
