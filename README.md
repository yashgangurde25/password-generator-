# CodeClauseInternship_Random Password Generator

This Python program generates random passwords based on user specifications.

## Program Explanation

```python
import random
import string

# Function to generate a random password
def generate_random_password(length=12):
    # Define the characters to use for generating the password
    characters = string.ascii_letters + string.digits + string.punctuation

    # Ensure the length is at least 8 characters
    if length < 8:
        length = 8

    # Generate a random password by selecting characters randomly
    password = ''.join(random.choice(characters) for _ in range(length))
    
    return password

if __name__ == "__main__":
    # Ask the user to enter the desired password length
    password_length = int(input("Enter the desired password length: "))
    
    # Generate a random password of the specified length
    password = generate_random_password(password_length)
    
    # Display the generated password to the user
    print("Generated Password:", password)

