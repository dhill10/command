# Function to convert a single word to Pig Latin
def word_to_pig_latin(word):
    # Check if the word is empty or contains non-alphabetic characters
    if not word.isalpha():
        return word  # Return the word as-is

    # Convert the word to lowercase (optional, but makes it consistent)
    word = word.lower()

    # Remove the first letter from the word
    first_letter = word[0]
    rest_of_word = word[1:]

    # Add the first letter to the end and append "ay"
    pig_latin_word = rest_of_word + first_letter + "ay"

    return pig_latin_word

# Function to convert a sentence to Pig Latin
def sentence_to_pig_latin(sentence):
    # Split the sentence into words
    words = sentence.split()

    # Convert each word to Pig Latin
    pig_latin_words = [word_to_pig_latin(word) for word in words]

    # Join the modified words to form the Pig Latin sentence
    pig_latin_sentence = " ".join(pig_latin_words)

    return pig_latin_sentence

# Input sentence
english_sentence = "I SLEPT MOST OF THE NIGHT"

# Convert the sentence to Pig Latin
pig_latin_result = sentence_to_pig_latin(english_sentence)

# Print the Pig Latin result
print("English:", english_sentence)
print("Pig Latin:", pig_latin_result)# command
