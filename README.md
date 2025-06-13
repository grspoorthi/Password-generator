Python 3.11.1 (tags/v3.11.1:a7a450f, Dec  6 2022, 19:58:39) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license()" for more information.
>>> KeyboardInterrupt
>>> import random
... import string
... 
... def generate_password(length):
...     # Define character sets for different complexity levels
...     lowercase_letters = string.ascii_lowercase
...     uppercase_letters = string.ascii_uppercase
...     digits = string.digits
...     special_characters = string.punctuation
... 
...     # Combine all character sets based on complexity
...     all_characters = lowercase_letters + uppercase_letters + digits + special_characters
... 
...     # Generate password randomly
...     password = ''.join(random.choice(all_characters) for _ in range(length))
...     return password
... 
... def main():
...     try:
...         # Prompt the user to specify the desired length of the password
...         length = int(input("Enter the desired length of the password: "))
...         
...         if length <= 0:
...             print("Password length must be greater than zero.")
...             return
... 
...         # Generate the password
...         password = generate_password(length)
... 
...         # Display the generated password
...         print("Generated Password:", password)
... 
...     except ValueError:
...         print("Please enter a valid integer for the password length.")
... 
... if __name__ == "__main__":
...     main()
