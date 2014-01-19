Installed
==============
installed: Distribute (Setuptools), Requests, Pip, Requests-Oauthlib, Twython



Basic
==============
python3 setup.py install #install .py file with python3

ctrl-C #break

iTerm is not happy with Unicode

pydoc at command line to see documentation, e.g. pydoc input #q to quit

from sys import argv #import 'argument variable' from the sys module (a.k.a. library)



Python vs. Python3
==============
python3 #start python3

print() vs. print #need parentheses

print("string and ", end=" ")
print("string")  #to have two have two long strings print on same line; bad form to have 80+ characters on line

input() vs. raw_input()


Formatters
==============

%s converts objects to string using str() #string
%r converts objects to string using repr() #raw string, returns result in Python syntax which can recreate object
%d formats a number for display #display

e.g.
>> d = datetime.date.today()
>> str(d)
'2011-05-14'
>> repr(d)
'datetime.date(2011, 5, 14)'



Misc
==============

print(""" bunch of text
here and 
here
""")  #to print multiple lines; can also use ''' if there are double-quotes being used elsewhere on the line

\some_character_here #escape sequences: how to put difficult-to-type characters into a string
e.g.
\\ #one backslash
\" #quote
\' #single quote
\r #carriage return
\n #adds a newline except when you use %r
\t #tab in

