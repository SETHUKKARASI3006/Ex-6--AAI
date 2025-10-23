<H3>NAME: SETHUKKARASI C</H3>
<H3>REGISTER NO.: 212223230201</H3>
<H3>EX. NO.6</H3>
<H3>DATE: 23-10-2025</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>
<H3>Aim: to perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques. </H3> 
 <BR>
<h3>Algorithm:</h3>
Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.
<H3>Program:</H3>

```
import nltk
#import wordnet
nltk.download( 'punkt_tab' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger_eng' )
sentence=input ()
# Print the parts of speech
for word, tag in pos_tags:
    print(word, tag)
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```

<H3>Output</H3>

<img width="592" height="148" alt="image" src="https://github.com/user-attachments/assets/2fcef356-c1ca-4577-9b39-010be831f684" />

<img width="467" height="32" alt="image" src="https://github.com/user-attachments/assets/a2f054a5-b19b-458d-af64-74c0923f8d96" />
<br>
<img width="145" height="240" alt="image" src="https://github.com/user-attachments/assets/4fcf170a-55e5-4278-bf4e-76bc8f8cd453" />

<img width="1732" height="65" alt="image" src="https://github.com/user-attachments/assets/d2106c88-e828-4a4b-b6de-4d04fd19f2c7" />

<H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
