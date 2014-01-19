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

python3 ex13.py first 2nd 3rd #call ex13.py with three arguments "first" "2nd" "3rd"

exit() #to exit python3; need parentheses

from os.path import exists #get the exists command

man some_command_here at command line #to get BSD Unix manual, e.g. man cat

cat filename at command line #easy way to print file to screen

python is case-sensitive



Python2 vs. Python3
==============
python3 #start python3

print() vs. print #need parentheses

print("string and ", end=" ")
print("string")  #to have two have two long strings print on same line; bad form to have 80+ characters on line

input() vs. raw_input() #also input is different from Python2 to Python3

integer division, e.g. 2/3, is now real division


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



Files
==============

txt = open(filename) #to open a file

txt = open(filename, 'w') #to open file in write mode, which overwrites the file; truncating not necessary then

txt.read() #to read a file

print txt.read() #to print the contents of the file

txt.close() #to close the file

txt.readline() #to read just one line

txt.truncate() #empties file

txt.truncate(let_comp_know_how_much_to_truncate) #truncate only part of file

txt.write(somethinghere) #to write to file

exists(filename) #check to see if file exists

filename.seek(0)  #go back to the beginning of file, to byte 0



Functions
==============

Functions do 3 things: name pieces of code, take arguments, let you make your own mini-scripts

def function_name(*args):  # *args is like argv but for functions; has to go inside ()

arg1, arg2 = args   #unpacks the arguments into separate variables

function headers head with a colon

the rest of the block is known through identation

function names can only have letters, numbers and underscores - and can't start with a number

you can pass functions constants, variables, and calculations

return some_value_here   #function will return this value



Misc
==============

print(""" bunch of text
here and 
here
""")  #to print multiple lines; can also use ''' if there are double-quotes being used elsewhere on the line

\some_character_here #escape sequences: how to put difficult-to-type characters into a string, need to be in quotes
e.g.
\\ #one backslash
\" #quote
\' #single quote
\r #carriage return
\n #adds a newline except when you use %r
\t #tab in

+=   #combines plus and equals, i.e. x = x + y is the same as x += y

