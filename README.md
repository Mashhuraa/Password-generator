#Password Generator

#Overwiev
--------------------------------
This repository contains a Python script that generates random passwords based on user-specified criteria. The user can choose to include uppercase letters, lowercase letters, digits, and symbols in the passwords. The script generates a specified number of passwords with a specified length.

Features
------------------------------------
1.Generates multiple passwords at once.

2.Customizable character types:

Uppercase letters (A-Z)

Lowercase letters (a-z)

Digits (0-9)

Symbols (!@#$%*&+_?/{}[]:;|\)

Ensures at least one type of character is selected.

Easily adjustable password length and number of passwords.

Usage
---------------------------
Clone the repository:

git clone https://github.com/yourusername/password-generator.git
cd password-generator

Customize the script:

Open password_generator.py and set the character types you want to include in your passwords by modifying the boolean variables:

use_uppercase = True

use_lowercase = True

use_digits = True

use_symbols = True

Set the number of passwords and their length:

Adjust the num_passwords and length variables as needed:

num_passwords = 5

length = 12

Run the script:

python password_generator.py

View the generated passwords:

The script will print the generated passwords to the console.

Example

Here is an example of the script generating 5 passwords, each 12 characters long, including all character types:

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

Generated Passwords:

4uRk&T1pVw*@

D2c#M3@ZfLg_

xF7!WpHs?8K9

Bq5+TsL1{mR2

6Za1Q%gP9*Fp

Customization
-------------------------------
To customize the script for your needs:

Character Types: Change the use_uppercase, use_lowercase, use_digits, and use_symbols variables to include or exclude certain types of characters.

Number of Passwords: Change the num_passwords variable to generate more or fewer passwords.

Password Length: Change the length variable to adjust the length of each generated password.

Notes
----------------------------------
The script ensures that at least one type of character is included. If no character types are selected, an exception is raised.
Adjust the character sets and variables as needed to fit your specific requirements.

License
-------------------------------
This project is licensed under the MIT License. See the LICENSE file for details.

Feel free to modify and enhance the script according to your needs. Happy password generating!

