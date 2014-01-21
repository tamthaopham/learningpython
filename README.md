Installed
==============
installed: Distribute (Setuptools), Requests, Pip, Requests-Oauthlib, Twython



Python2 vs. Python3
==============
python3 #start python3

print() vs. print #need parentheses

print("string and ", end=" ")
print("string")  #to have two have two long strings print on same line; bad form to have 80+ characters on line

input() vs. raw_input() #also input is different from Python2 to Python3

integer division, e.g. 2/3, is now real division

complex expressions in flow control statements (e.g. while) have to be in parentheses

urllib module, import urllib.request vs. urllib to use urlopen; call by urlopen(URL).readlines()

list(dict_keys()) vs. dict_keys() for indexing, i.e. to use keys as list

super().__init__() vs. super(ChildB, self).__init__() # inside init function, allows you to run the init method of a parent class reliably, mostly useful for multiple inheritances


Basic
==============
comment with hashtags

documentation comments come after on the line below function header between """ and """

help(filename) will display the documentation comments for each function in the file
help(filename.function_name) will display the documentation comment for the function

python3 setup.py install #install .py file with python3

pip install <packagename>

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

import module_name  # imports module (in the same directory, no .py extension) but you still have to refer to the module_name when calling its functions, e.g. module_name.function_name()

from module_name import *    # imports all functions and you no longer have to refer to module_name when calling its functions, e.g. function_name()

import module_name as mdl_nm    # use as to give modules an alias when importing
e.g. mdl_nm.randint(0,10)

classes don't interfere with each other, while with modules, when you import there is generally only one for the entire program

instead of importing, you INSTANTIATE a class, to get what is called an object, e.g.
  thing = MyStuff()    # equivalent to set thing to an instance of MyStuff 
  thing.apple(J)        # from the class MyStuff, get the function apple that takes parameters self and J
  thing.tangerine = K   # take attribute tangerine from thing and assign to K

class X(Y)  # equivalent to 'make a class X that is-a Y' 

you can automatically INITIALIZE an object of a class, e.g. 
  def __init__(self, lyrics):         # object is passed the class object parameters (when called) as well as itself
      self.tangerine = "And now a thousand years in-between"  # self is the empty object made by Python
      self.lyrics = lyrics
      self.pet = None     # initialize attribute without assignment, None is a python term

functions in classes are passed self as object

dir()    # used to find out which names (relevant attributes) a module defines (but not built-in functions & variables, returns a sorted list of strings




Variables & Types
==============

variable types don't need to be declared; Python figures out types on its own

mutable objects can be changed after they're created (e.g. lists)

immutable objects cannot be changed (e.g. strings, tuples, integers, etc)
  - when you change a string, you are actually binding the variable to a different newly created object
  - why string concatenation is slow and expensive, it requires making many copies, while appending to a list is cheap
  - it's the bindings that are immutable, not the objects (so if you can change the underlying object, then you can also change what the variable refers to, e.g. tuples)

global globvar    # declaration of intent to change global variable inside a function; considered dangerous

Data Types:  True, False, None, Strings, Integer (default for numbers), Floats (Decimal), Lists

string_name.join(collection_name) # join is a method of string that allows the string_name to serve as a "joiner" of the items in the collection




Text
==============

double quotes and single quotes can be used almost interchangeably

lone unmatched double quotes or single quotes can be used inside the text between a matched pair

""" should be used when there is both a double and single quote inside the text

print(""" bunch of text
here and 
here
""")  #to print multiple lines; can also use ''' if there are double-quotes being used elsewhere on the line

words = sentence.split(" ")  #split some variable string called sentence into a list by the " " delimiter
                             Does not affect the string variable

sorted(words)  #sorts a list; if alphabetical, capitalized letters come first

print(text_to_be_printed)   

\ is used to prematurely end a line of code and pick up on the next, e.g. 
if a == True and \
   b == False



Logical Operands
==============

Truth Terms:  and, or, not, != or <>, ==, >, >=, <, <=, True, False

Less Intuitive Logic
  False or True = True
  False or False = False
  True and False = False
  False and False = False
  # note that the expression returned is actually one of the operands, the last operand required to conclude the result
      - False and anything returns False
      - True or anything returns the first operand

x in list_name    # test to see if item in list
substring in string_name   # test to see if substring in string

is      # a is b tests to see whether both are bound to the same object; different than equal, because a could == b and not a is b


Other Operators
==============

Standard: + , - , * , / 

=   #assignment

%    #mod (remainder)

**  #exponent

//  #floor (round-down) division

+=   #combines plus and equals, i.e. x = x + y is same as x += y, almost like an append; a.k.a increments by operator

-=   #subtracts and assigns, a -= b is the same as a = a - b

*=   #multiplies and assigns, a *= b is the same as a = a * b

/=   #divides and assigns, a /= b is the same as a = a / b

%=   #mod and assigns, a %= b is the same as a = a mod b

**=  #exponent  and assigns, a **= b is the same as a = a ** b

//=  #floor division and assigns, a //= b is the same as a = a // b

[ ]  #used for array items 

( )  #used for function operators

:    #end of header line for blocks

.    #used to connect object to function when calling

,    #used to separte items, e.g. print(a, b)

;    #only used for multiple statements on the same line

@    #class, function and method decorators, e.g. @property

{ }  #used to define a dictionary

_    #leading underscore on a name in a class is intended to indicate that the class is private (convention)

__   #leading double-underscore is intended to name-mangle so the system won't use names that conflict

__a__ #leading and trailing double-underscore is intended for builtin methods or variables




Formatters
==============

%s converts objects to string using str() #string
%r converts objects to string using repr() #raw string, returns result in Python syntax which can recreate object
%d formats a number for display #display

%i signed integer decimal
%o unsigned octal
%u unsigned decimal
%x unsigned hexidecimal (lowercase)
%X unsigned heixidecimal (uppercase)
%e floating point exponential (lowercase)
%E floating point exponential (uppercase)
%f floating point decimal
%F floating point decimal 
%g flaoting point format
%G floating point format
%c single character, integer or char
%% no argument converted, results in %



e.g.
>> d = datetime.date.today()
>> str(d)
'2011-05-14'
>> repr(d)
'datetime.date(2011, 5, 14)'



Collections
==============

An iterable is something you can iterate through and read, i.e. you can use for, while, in:  strings, lists, files

Collections in python use cardinal numbers (starts with zero, e.g. like cards in a deck that can be drawn at random) rather than ordinal numbers (starting with 1, e.g. ordered as in a race)

range(0,5)  # begins at 0 and slicing off BEFORE 5, i.e. 0, 1, 2, 3, 4

range(0,6,2)  # begins at 0, incrementing by 2, and slicing off BEFORE 6, i.e. 0, 2, 4

len(range(0,x) = x  # length of range from 0 is the same as maximum

len(range(a,b) = b - a  # length of range is the same as distance between range, i.e. not off by one

range(a,a) = []   # there is no distance between a number and itself

range(a,b) + range(b,c) = range(a,c)  # you can add two ranges and come up with an intuitive result:  note that range(a,b) does not include b and range(b,c) does

n % m in range m   # remainder of n div m is a positive integer less than m (i.e. in range(0,m))

list_name = ['something', 5, a]    # create a list
list_name = range(0,6)             # create a list from a range, i.e. 0, 1, 2, 3, 4, 5
list_name.extend(range(0,6))       # takes a list argument
list_name()                        # initialize list
list_name.append(single_item)      # takes a single argument
item = list[index_num]             # reference a single item in list
del list_name[index]               # remove item from list by index
del list_name[a:b]                 # remove part of list by range
word = words.pop(0)                # pops off a list the item at the index

# lists are mutable and can be changed in place 

other list methods: list(iterable), add, contains, delitem, delslice, eq, ge, getattribute, getitem, getslice, gt, iadd, + , * , insert, index, count, remove, reverse, sort, in

list2x2 = [[1,2,3],[4,5,6]]   # example of 2-dimensional list, i.e. list of lists

for item in collection:    # repeat loop for each item in collection

dictionaries (a.k.a. hashes)
  e.g. stuff = {'name':'Zed','age':36}
  therefore, stuff['name'] == 'Zed'
  assign by, stuff[1] = "Wow"    # assigns "Wow" to the key that 1 as value  (not ordered)
  delete, del stuff['city]
  return value, dict_name.get(key, default_value_to_be_returned_if_key_does_not_exist=None)


Flow Control
==============

if <expression>:        # for good style, every if should have an else that's either comprehensive or die
elif <expression>:      # avoid nested if statements, max. 2 deep
else:

for item in collection:  # repeat loop for each item in collection
                         # can use a variable that has not been initialized since it defines the variable
                         # preferred over while loops

from sys import exit     # import exit command
exit(0)                  # exit program; index indicates the type of error, 0 = good exit
break                    # break out of loop
continue                 # move to next loop
assert(bool_exp)         # tests if expression is true, otherwise program ends

while (<expression>): # repeat loop while expression holds true; can result in infinite loops
                      # often needs parentheses if expression is complex
while True:           # loops forever
                      # generally avoid using while unless you want it to loop forever, which means rarely

try:                  # exception handling; try block continues until exception, then moves to except block
except ErrorType      # error types are specific, e.g. ValueError, and only caught here if they match
except IOError as e   # example of an alias for exception handling, e.g. print("I/O error({0}): {1}".format(e.errno, e.strerror))

raise                 # raise either a non-syntactical programmer error, e.g. raise error ("Ouch!", or re-raise current error to be handled up the stack, e.g. raise or raise ErrorType() inside an except block

finally:              # used to make sure the block is executed no matter what, even if exceptions are caught in an earlier block, e.g. filename.close()

pass                  # null operation, used as a stand-in, e.g. def f(arg): pass #does nothing (yet)





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
yield some_generator_here #function will return a generator, e.g. i*i

exec expression   # allows for dynamic execution of expression

lambda is used for very short functions that you don't want to name, e.g. applier(lambda z: z * 4, 7)



Classes
==============

class class_name:   # class definition



Escape Sequences
==============

\some_character_here #escape sequences: how to put difficult-to-type characters into a string, need to be in quotes
e.g.
\\ #one backslash
\" #quote
\' #single quote
\r #carriage return
\n #adds a newline except when you use %r
\t #tab in
\a #bell
\b #backfeed
\f #formfeed
\v #vertical tab










