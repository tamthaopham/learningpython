Installed
==============
installed: Distribute (Setuptools), Requests, Pip, Requests-Oauthlib, Twython



Basic
==============
python3 setup.py install # install .py file with python3



Python vs. Python3
==============
python3 #start python3

print() vs. print #need parentheses

print("string and ", end=" ")
print("string")  #to have two have two long strings print on same line; bad form to have 80+ characters on line



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

\n adds a newline except when you use %r
