Installed
==============
installed: Distribute (Setuptools), Requests, Pip, Requests-Oauthlib, Twython



Basic
==============
comment with hashtags

documentation comments come after on the line below function header between """ and """

help(filename) will display the documentation comments for each function in the file
help(filename.function_name) will display the documentation comment for the function

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

python is generally a reference language, i.e. foo = Foo() means that foo is Foo()'s name and if x is also used to refer to Foo(), then if it changes, what both foo and x refers to will change

everything in python is an object

import module_name  # imports module but you still have to refer to the module_name when calling its functions, e.g. module_name.function_name()

from module_name import *    # imports all functions and you no longer have to refer to module_name when calling its functions, e.g. function_name()



Logical Operands
==============

Truth Terms:  and, or, not, !=, ==, >=, <=, True, False

Less Intuitive Logic
  False or True = True
  False or False = False
  True and False = False
  False and False = False
  # note that the expression returned is actually one of the operands, the last operand required to conclude the result
      - False and anything returns False
      - True or anything returns the first operand




Python2 vs. Python3
==============
python3 #start python3

print() vs. print #need parentheses

print("string and ", end=" ")
print("string")  #to have two have two long strings print on same line; bad form to have 80+ characters on line

input() vs. raw_input() #also input is different from Python2 to Python3

integer division, e.g. 2/3, is now real division



Text
==============

words = sentence.split(" ")  #split some variable string called sentence into a list by the " " delimiter
                             Does not affect the string variable

sorted(words)  #sorts a list; if alphabetical, capitalized letters come first


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

+=   #combines plus and equals, i.e. x = x + y is same as x += y, almost like an append; a.k.a increments by operator

lambda is used for very short functions that you don't want to name, e.g. applier(lambda z: z * 4, 7)

mutable objects can be changed after they're created (e.g. lists)

immutable objects cannot be changed (e.g. strings, tuples, integers, etc)
  - when you change a string, you are actually binding the variable to a different newly created object
  - why string concatenation is slow and expensive, it requires making many copies, while appending to a list is cheap
  - it's the bindings that are immutable, not the objects (so if you can change the underlying object, then you can also change what the variable refers to, e.g. tuples)

word = words.pop(0)  # pops off a list the item at the index

