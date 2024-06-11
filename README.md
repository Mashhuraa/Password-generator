# Password-generator

#Overview
-----------------------------------
This Python script generates random passwords based on user-specified criteria. The user can choose to include uppercase letters, lowercase letters, digits, and symbols in the passwords. The script will generate a specified number of passwords with a specified length.

Features
Generates multiple passwords at once.
Customizable to include:
Uppercase letters (A-Z)
Lowercase letters (a-z)
Digits (0-9)
Symbols (!@#$%*&+_?/{}[]:;|\)
Ensures at least one type of character is selected.
Easily adjustable password length and number of passwords.
Prerequisites
Python 3.x
How to Use
Set the character types you want to include in your passwords by modifying the boolean variables:

use_uppercase: Set to True to include uppercase letters.
use_lowercase: Set to True to include lowercase letters.
use_digits: Set to True to include digits.
use_symbols: Set to True to include symbols.
Set the number of passwords you want to generate by changing the num_passwords variable.

Set the length of each password by changing the length variable.

Run the script. The script will generate the specified number of passwords and print them to the console.

Example
Here is an example of the script generating 5 passwords, each 12 characters long, including all character types:

python
Copy code
import random

uppercase_letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
lowercase_letters = "abcdefghijklmnopqrstuvwxyz"
digits = "0123456789"
symbols = "!@#$%*&+_?/{}[]:;|\\"

characters = ""
use_uppercase = True
use_lowercase = True
use_digits = True
use_symbols = True

if use_uppercase:
    characters += uppercase_letters
if use_lowercase:
    characters += lowercase_letters
if use_digits:
    characters += digits
if use_symbols:
    characters += symbols

if not characters:
    raise Exception("At least one character type must be chosen.")

num_passwords = 5
length = 12

passwords = []
for _ in range(num_passwords):
    password = "".join(random.choices(characters, k=length))
    passwords.append(password)

print("\nGenerated Passwords:")
for password in passwords:
    print(password)
Output
perl
Copy code
Generated Passwords:
4uRk&T1pVw*@
D2c#M3@ZfLg_
xF7!WpHs?8K9
Bq5+TsL1{mR2
6Za1Q%gP9*Fp
Customization
To customize the script for your needs:

Character Types: Change the use_uppercase, use_lowercase, use_digits, and use_symbols variables to include or exclude certain types of characters.
Number of Passwords: Change the num_passwords variable to generate more or fewer passwords.
Password Length: Change the length variable to adjust the length of each generated password.
Notes
The script ensures that at least one type of character is included. If no character types are selected, an exception is raised.
Adjust the character sets and variables as needed to fit your specific requirements.
License
This script is provided as-is without any warranties or guarantees. Use at your own risk.

