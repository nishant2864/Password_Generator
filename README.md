# CodeAlpha__Password_Generator
# Here's a simple Python script for a password generator that generates random and strong passwords with a mix of alphabets, numbers, and special characters. 

import random
import string

def generate_password(length=12):
    # Define character sets for different types of characters
    lowercase_letters = string.ascii_lowercase
    uppercase_letters = string.ascii_uppercase
    digits = string.digits
    special_characters = "!@#$%^&*()_+=-[]{}|;:'<>,.?/~"

    # Combine all character sets
    all_characters = lowercase_letters + uppercase_letters + digits + special_characters

    # Ensure the password length is at least 8 characters
    length = max(length, 8)

    # Generate the password using random.choices
    password = ''.join(random.choices(all_characters, k=length))

    return password

if __name__ == "__main__":
    password_length = int(input("Enter the desired password length: "))
    generated_password = generate_password(password_length)
    print("Generated Password:", generated_password)
