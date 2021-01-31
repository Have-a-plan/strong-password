# strong-password
Exercise 
import re

password = input('Enter the password: ')

h1 = re.compile(r'[A-Z]')
h2 = re.compile(r'[a-z]')
h3 = re.compile(r'[0-9]')

while True:
    if len(password) < 8:
        print(len(password))
        print('This password not secure')
        password = input('Enter the password: ')
        continue
    elif len(h1.findall(password)) == 0:
        print(len(h1.findall(password)), 'h1')
        print('This password not secure')
        password = input('Enter the password: ')
        continue
    elif len(h2.findall(password)) == 0:
        print(len(h2.findall(password)), 'h2')
        print('This password not secure')
        password = input('Enter the password: ')
        continue
    elif len(h3.findall(password)) == 0:
        print(len(h3.findall(password)), 'h3')
        print('This password not secure')
        password = input('Enter the password: ')
        continue
    else: break
    

    
print('Password was saved', password)    
