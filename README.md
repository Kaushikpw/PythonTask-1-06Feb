#Q2. Write a python program for encrypting a message sent to you by your friend. The logic of encryption
#should be such that, for a the output should be z. For b, the output should be y. For c, the output should
#be x respectively. Also, the whitespace should be replaced with a dollar sign. Keep the punctuation
#marks unchanged.
#Input Sentence: I want to become a Data Scientist.
#Encrypt the above input sentence using the program you just created.
#Note: Convert the given input sentence into lowercase before encrypting. The final output should be
#lowercase.

#Ans.:

def encrypt_message(message):
    encrypted_message = ""
    for char in message:
        if char.isalpha():
            encrypted_message += chr(219 - ord(char))
        elif char.isspace():
            encrypted_message += "$"
        else:
            encrypted_message += char
    return encrypted_message

# Input sentence
sentence = "I want to become a Data Scientist.".lower()

# Encrypt the sentence
encrypted_sentence = encrypt_message(sentence)
print(encrypted_sentence)

def product_of_elements(lst):
    product = 1
    for el in flatten(lst):
        if isinstance(el, int) or isinstance(el, float):
            product *= el
    return product

list1 = [1,2,3,4, [44,55,66, True], False, (34,56,78,89,34), {1,2,3,3,2,1}, {1:34, "key2": [55, 67, 78, 89], 4: (45, 22, 61, 34)}, [56, 'data science'], 'Machine Learning']

print(product_of_elements(list1))
