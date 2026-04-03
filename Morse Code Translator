# this is in python!
# by me!

import time
morse_code_dict = {
    # Letters
    'A': '.-',   'a': '.-',
    'B': '-...', 'b': '-...',
    'C': '-.-.', 'c': '-.-.',
    'D': '-..',  'd': '-..',
    'E': '.',    'e': '.',
    'F': '..-.', 'f': '..-.',
    'G': '--.',  'g': '--.',
    'H': '....', 'h': '....',
    'I': '..',   'i': '..',
    'J': '.---', 'j': '.---',
    'K': '-.-',  'k': '-.-',
    'L': '.-..', 'l': '.-..',
    'M': '--',   'm': '--',
    'N': '-.',   'n': '-.',
    'O': '---',  'o': '---',
    'P': '.--.', 'p': '.--.',
    'Q': '--.-', 'q': '--.-',
    'R': '.-.',  'r': '.-.',
    'S': '...',  's': '...',
    'T': '-',    't': '-',
    'U': '..-',  'u': '..-',
    'V': '...-', 'v': '...-',
    'W': '.--',  'w': '.--',
    'X': '-..-', 'x': '-..-',
    'Y': '-.--', 'y': '-.--',
    'Z': '--..', 'z': '--..',

    # Numbers
    '0': '-----',
    '1': '.----',
    '2': '..---',
    '3': '...--',
    '4': '....-',
    '5': '.....',
    '6': '-....',
    '7': '--...',
    '8': '---..',
    '9': '----.',

    # Punctuation and special characters
    '.': '.-.-.-',
    ',': '--..--',
    '?': '..--..',
    "'": '.----.',
    '!': '-.-.--',
    '/': '-..-.',
    '(': '-.--.',
    ')': '-.--.-',
    '&': '.-...',
    ':': '---...',
    ';': '-.-.-.',
    '=': '-...-',
    '+': '.-.-.',
    '-': '-....-',
    '_': '..--.-',
    '"': '.-..-.',
    '$': '...-..-',
    '@': '.--.-.'
}

def text_to_morse(text):
    morse_chars = []
    for char in text:
        if char == " ":
            morse_chars.append("/")
        elif char in morse_code_dict:
            morse_chars.append(morse_code_dict[char])
        else:
            morse_chars.append('?')
    return " ".join(morse_chars)

def morse_to_text(morse):
    # Helper function: Given a Morse symbol, return the corresponding character.
    def get_char(morse_symbol):
        # First, prefer uppercase characters.
        for char, code in morse_code_dict.items():
            if code == morse_symbol and char.isupper():
                return char
        # If no uppercase letter is found, return the first available match.
        for char, code in morse_code_dict.items():
            if code == morse_symbol:
                return char
        return ''  # unknown symbol

    # Assume words are separated by "/" and letters by spaces.
    words = morse.strip().split("/")
    decoded_words = []
    for word in words:
        letters = word.strip().split()
        decoded_letters = [get_char(letter) for letter in letters]
        decoded_words.append(''.join(decoded_letters))
    return ' '.join(decoded_words)

# Interactive menu for the translator.
print("Welcome To the Morse Code Translator!"
      "\n1. text --> morse code"
      "\n2. morse code --> text"
      "\n3. exit")
while True:
    menu = input("Choose an option (1, 2, or 3): ")

    if menu == "1":
        inputted_text = input("What text would you like to translate? (example: 'Hello, World!'): ")
        print(f"\n{text_to_morse(inputted_text)} (the slash(es) mean space)")
    elif menu == "2":
        inputted_text = input("What morse code would you like to translate? "
                              "\n(example: '.... . .-.. .-.. --- --..-- / .-- --- .-. .-.. -.. -.-.--'): ")
        print(f"\n{morse_to_text(inputted_text)}")
    elif menu == "3":
        print("Exiting the translator...")
        time.sleep(2)
        print("Goodbye!")
        quit()
    else:
        print("Invalid option. Please restart and choose 1, 2, or 3.")
