# password-generator
This code will generates 200 passwords for the 200 users with uppercase,lowercase,numbers and special characters in it and the length of the password is of 8
import random
import string

x = string.ascii_uppercase+string.ascii_lowercase+string.digits+string.punctuation

lst = []

while len(lst) < 200:
    rand_val = random.choices(x, k=8)
    lc = 0;uc = 0;dc = 0;pc = 0
    for k in rand_val:
        if k.isupper() == True:
            uc = 1
        elif k.islower() == True:
            lc = 1
        elif k.isdigit() == True:
            dc = 1
        else:
            pc = 1
    if lc == 1 and uc ==1 and dc == 1 and pc == 1:
        lst.append("".join(rand_val))
    
    
print(lst)
print(len(lst))
