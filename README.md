# Verses-Unleashed_N-gram-Poetry-Generation-Project

The task is to generate a poem using different models. We will generate a poem verse by verse until all stanzas have been generated. The poetry generation problem can be solved using the following algorithm:

1-Load the Poetry Corpus
2-Tokenize the corpus in order to split it into a list of words
3-Generate n-gram models
4-For each of the stanzas – For each verse
5-Generate a random number in the range [7...10]
6-Select first word
7-Select subsequent words until end of verse
8-[bonus] If not the first verse, try to rhyme the last word with the last word of the previous verse
9-Print verse – Print empty line after stanza 2.1 Implementation Challenges:
Among the challenges of solving this assignment will be selecting subsequent words once we have chosen the first word of the verse. To predict the next word, what we aim to compute is the most probable next word from all the possible next words. In other words, we need to find the set of words that occur most frequently after the already selected word and choose the next word from that set. We can use a Conditional Frequency Distribution (CFD) to figure that out! A CFD tells us: given a condition, what is likelihood of each possible outcome. [bonus] Rhyming the generated verses is also a challenge. You can build your dictionary for rhyming. The Urdu sentence is written from right to left, so makes your n-gram models according to this style.

2.2 Standard n-gram Models We can develop our model using the Conditional Frequency Distribution method. First develop a unigram model (Unigram Model), then the bigram model (Bigram Model) and then trigram model. Select the first word of each line randomly from starting words in the vocabulary and then use the bigram model to generate the next word until the verse is complete. Generate the next three lines similarly. Follow the same steps for the trigram model and compare the results of the two n-gram models.
