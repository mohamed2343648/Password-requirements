# A program in which the user enters the password icludes the following conditions :
# It must contain at least one number
# It must contain at least one capital letter and one small letters
# It must contain at least one symbol
# Password length does not exceed 12 and not less than 6

import re
code = ' '
def mot_de_pass(password):
    password = (input("enter your password:  "))
    number = re.findall("[0-9]", password)
    capital = re.findall("[A-Z]", password)
    small = re.findall("[a-z]", password)
    char = re.findall("[#. @!?]", password)
    size = len(password)
    print("the size of password is: ", size)
    if not size <= 12 and size >= 6:
        print("the length of password must be between (6 to 12) characters")
        return mot_de_pass(password)
    if not capital:
        print("the password must contain at least one capital letter")
        return mot_de_pass(password)
    if not number:
        print("the password must contain at least one number")
        return mot_de_pass(password)
    if not small:
        print("the password must contain at least one small letter")
        return mot_de_pass(password)
    if not char:
        print("the password must contain a special character")
        return mot_de_pass(password)
    else :
        print("Excellent Choice!! your password is accepted: ", password)
mot_de_pass(code)
