			====================================
					String Handling Part-2
				====================================
=>We know that, on str data we can perform Both Indexing and Slicing Operations.
=>By using Indexing Concept, we can get Single Value from str object.
=>By using Slicing Concept, we can get Range of Values  from str object.
=>Along with Indexing and Slicing Operations, we can perform Various Operations on str data by using Pre-defined Functions 
   present in str object.
--------------------------------------------------------------------------------------------------------------------------------
Pre-defined Functions in str object
--------------------------------------------------------------------------------------------------------------------------------
1) capitalize()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function is used for capitalizing the first letter First word of a given Sentence only.
=>Syntax:      strobj.capitalize()
				(OR)
			strobj=strobj.capitalize()
-----------------
Examples:
-----------------
>>> s="python"
>>> print(s,type(s))-------------------python <class 'str'>
>>> s.capitalize()--------------------'Python'
>>> s="python is an oop lang"
>>> print(s,type(s))-------------------------python is an oop lang <class 'str'>
>>> s.capitalize()-----------------------------'Python is an oop lang'
-------------------------------------
>>> s="python"
>>> print(s,type(s))--------------------python <class 'str'>
>>> s.capitalize()--------------------'Python'
>>> print(s,type(s))----------------python <class 'str'>
>>> s=s.capitalize()
>>> print(s,type(s))-----------------Python <class 'str'>
--------------------------------------------------------------------------------------------------------------------------------
2) title():
--------------------------------------------------------------------------------------------------------------------------------
=>This is used for obtaining Title Case of a Given Sentence  (OR) Making all words First 
    Letters are capital.
Syntax:          s.title()
			(OR)
			s=s.title()
	
------------------
Examples:
------------------
>>> s="python"
>>> print(s,type(s))-------------------python <class 'str'>
>>> s.capitalize()---------------------'Python'
>>> s.title()-----------------------------'Python'
----------------------------------------------------------
>>> s="python is an oop lang"
>>> print(s,type(s))------------------python is an oop lang <class 'str'>
>>> s.capitalize()--------------------'Python is an oop lang'
>>> s.title()----------------------------'Python Is An Oop Lang'
>>> print(s)----------------------------python is an oop lang
>>> s=s.title()
>>> print(s)--------------------------Python Is An Oop Lang
--------------------------------------------------------------------------------------------------------------------------------
3) index()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function obtains Index of the specified Value
=>If the specified value does not exist then we get ValueError
=>Syntax:        strobj.index(Value)
=>Syntax:	indexvalue=strobj.index(value)

Examples:
-----------------
>>> s="python"
>>> s.index("p")------------------0
>>> s.index("y")-------------------1
>>> s.index("o")-----------------4
>>> s.index("n")----------------5
>>> s.index("K")----------------ValueError: substring not found

--------------------------------------------------------------------------------------------------------------------------------
4) upper()
--------------------------------------------------------------------------------------------------------------------------------
=>It is used for converting any type of Str Data into Upper Case.
=>Syntax:-   strobj.upper()
			OR
			strobj=strobj.upper()
-----------------
Examples:
=---------------
>>> s="python"
>>> print(s)------------------------------python
>>> s.upper()-----------------------'PYTHON'
>>> s="python is an oop lang"
>>> print(s)---------------------------------python is an oop lang
>>> s.upper()--------------------------------'PYTHON IS AN OOP LANG'
>>> s="Python IS  an OOP lang"
>>> print(s)-------------------------------Python IS  an OOP lang
>>> s.upper()--------------------------'PYTHON IS  AN OOP LANG'
>>> s="AbCdEf"
>>> print(s)------------------------AbCdEf
>>> s.upper()----------------------'ABCDEF'
>>> s="PYTHON"
>>> print(s)--------------------PYTHON
>>> s.upper()-----------------'PYTHON'
>>> s="123"
>>> print(s)------------------123
>>> s.upper()----------------'123'
--------------------------------------------------------------------------------------------------------------------------------
5) lower()
--------------------------------------------------------------------------------------------------------------------------------
=>It is used for converting any type of Str Data into lower Case.
=>Syntax:-   strobj.lower()
			OR
			strobj=strobj.lower()
Examples:
-----------------
>>> s="Data Science"
>>> print(s)--------------Data Science
>>> s.lower()------------'data science'
>>> s="python"
>>> print(s)-------------python
>>> s.lower()-----------'python'
>>> s="PYTHON"
>>> print(s)-------------PYTHON
>>> s.lower()------------'python'
>>> s="PYThon"
>>> print(s)----------PYThon
>>> s.lower()---------'python'
--------------------------------------------------------------------------------------------------------------------------------
6) isupper()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided the given str object data is purely Upper Case otherwise it returns False.
Syntax:     strobj.isupper()

Examples:
-----------------
>>> s="PYTHON"
>>> s.isupper()-----------True
>>> s="python"
>>> s.isupper()----------False
>>> s="Python"
>>> s.isupper()----------False
>>> s="PYThon"
>>> s.isupper()----------False
>>> s="123"
>>> s.isupper()------------False
>>> s="%$#^&@"
>>> s.isupper()-----------False

--------------------------------------------------------------------------------------------------------------------------------
7)islower()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided the given str object data is purely lower Case otherwise it returns False.
	Syntax:     strobj.islower()
-----------------
Examples:
-----------------
>>> s="pythopn"
>>> s.islower()------------True
>>> s="pythOn"
>>> s.islower()------------False
>>> s="PYTHON"
>>> s.islower()-----------False
>>> s="123"
>>> s.islower()----------False
--------------------------------------------------------------------------------------------------------------------------------
8) isalpha()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided str object contains Purely Alphabets otherwise returns False.

		Syntax:   strobj.isalpha()
-------------------
Examples:
-------------------
>>> s="Ambition"
>>> s.isalpha()--------------------True
>>> s="Ambition123"
>>> s.isalpha()-------------------False
>>> s="1234"
>>> s.isalpha()------------------False
>>> s="   "
>>> s.isalpha()------------------False
>>> s="#$%^@"
>>> s.isalpha()-----------------False
>>> s="AaBbZz"
>>> s.isalpha()----------------True
--------------------------------------------------------------------------------------------------------------------------------
9) isdigit()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided given str object contains purely digits otherwise returns False
Examples:
--------------------
>>> s="python"
>>> s.isdigit()------------------False
>>> s="python123"
>>> s.isdigit()----------------False
>>> s="123"
>>> s.isdigit()-----------------True
>>> s="123 456"
>>> s.isdigit()---------------False
>>> s="1_2_3"
>>> s.isdigit()---------------False
>>> s="123KV"
>>> s.isdigit()-------------False
--------------------------------------------------------------------------------------------------------------------------------
10) isalnum()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided str object contains either Alpabets OR Numerics or Alpha-Numerics only otherwise It returns False.
	=>Syntax:   strobj. isalphanum()
---------------------------
=>Examples:
---------------------------
>>> s="python310"
>>> s.isalnum()-----------------True
>>> s="python"
>>> s.isalnum()-----------------True
>>> s="310"
>>> s.isalnum()-----------------True
>>> s="$python310"
>>> s.isalnum()-----------------False
>>> s="python 310"
>>> s.isalnum()----------------False
>>> s="$python3.10"
>>> s.isalnum()----------------False
>>> s="python3.10"
>>> s.isalnum()-------------False
-------------------------------------------------------------------------------------------------------------------------------
11) isspace()
-------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided str obj contains purely space otherwise it returns False.
=>Syntax:    strobj.isspace()
------------------------
Examples:
----------------------
>>> s="  "
>>> s.isspace()-----------True
>>> s=""
>>> s.isspace()--------------False
>>> s="python Prog"
>>> s.isspace()-------------False
>>> s="Prasana Laxmi"
>>> s.isspace()--------------False
>>> s.isalpha()-----------False
>>> s.isalpha() or s.isspace()-----------False
-------------------------------------------------------------------------------------------------------------------------------
12) split()
-------------------------------------------------------------------------------------------------------------------------------
=>This Function is used for splitting the given str object data into different words base specified delimter ( -  _  # % ^ ^ , ; ....etc)
=>The dafeult deleimter is space 
=>The Function returns Splitting data in the form of list object
=>Syntax:    strobj.split("Delimter")
				(OR)
			strobj.split()
				(OR)
			listobj=  strobj.split("Delimter")
				(OR)
			listobj=strobj.split()
----------------
Examples:
----------------
>>> s="Python is an oop lang"
>>> print(s)----------------Python is an oop lang
>>> s.split()----------------['Python', 'is', 'an', 'oop', 'lang']
>>> len(s.split())-----------5
>>> x=s.split()
>>> print(x,type(x))---------['Python', 'is', 'an', 'oop', 'lang'] <class 'list'>
>>> len(x)---------------5
>>> s="12-09-2022"
>>> print(s)-------------12-09-2022
>>> s.split("-")----------['12', '09', '2022']
>>> s="12-09-2022"
>>> dob=s.split("-")
>>> print(dob,type(dob))------------['12', '09', '2022'] <class 'list'>
>>> print("Day",dob[0])----------Day 12
>>> print("Month ",dob[1])---------Month  09
>>> print("Year ",dob[2])----------Year  2022
---------------------------------------------------------
>>> s="Apple#Banana#kiwi/Guava"
>>> words=s.split("#")
>>> print(words)-----------['Apple', 'Banana', 'kiwi/Guava']
>>> words=s.split("/")
>>> print(words)------------------['Apple#Banana#kiwi', 'Guava']
-------------------------------------------------------------------------------
13) join():
-------------------------------------------------------------------------------
=>This Function is used for combining or joining list of values from any Iterable object
=>Syntax:    strobj.join(Iterableobject)
Examples:
------------------------------
>>> lst=["HYD","BANG","AP","DELHI"]
>>> print(lst,type(lst))------------------['HYD', 'BANG', 'AP', 'DELHI'] <class 'list'>
>>> s=""
>>> s.join(lst)---------------'HYDBANGAPDELHI'
>>> s=" "
>>> s.join(lst)------------------'HYD BANG AP DELHI'
-------------------------------------------------------------------
>>> t=("Rossum","is", "Father" "of" ,"Python")
>>> print(t,type(t))
('Rossum', 'is', 'Fatherof', 'Python') <class 'tuple'>
>>> k=" "
>>> k.join(t)
'Rossum is Fatherof Python'
>>> t=("Rossum","is", "Father", "of" ,"Python")
>>> k=" "
>>> k.join(t)
'Rossum is Father of Python'
---------------------------------------------------------------------------------------------------------------------
14) startswith():
----------------------
=>The startswith() Function returns True if the string starts with the specified value, otherwise False.
Examples:
-------------------
>>>s="Python is an oop lang"
>>>s.startswith("Python")------------True
>>>s.startswith("python")------------False
---------------------------------------------------------------------------------------------------------------------
15) endswith():
----------------------
=>The endswith() Function returns True if the string ends with the specified value, otherwise False.
Examples:
-------------------
>>>s="Python is an oop lang"
>>>s.endswith("Python")------------False
>>>s.endswith("lang")------------True
---------------------------------------------------------------------------------------------------------------------
16) swapcase()
----------------------------
=>Make the lower case letters upper case and the upper case letters lower case:
Examples:
>>>s="PyThOn"
>>>s.swapcase()--------pYtHoN
---------------------------------------------------------------------------------------------------------------------
MISc Examples
---------------------------------------------------------------------------------------------------------------------
>>> s="python"
>>> s.capitalize()
'Python'
>>> s="python is an oop lang"
>>> s.capitalize()
'Python is an oop lang'
>>> s="python is an oop lang.python is also fun lang"
>>> s.capitalize()
'Python is an oop lang.python is also fun lang'
>>>
>>> s="python"
>>> s.title()
'Python'
>>> s="python is an oop lang"
>>> s.title()
'Python Is An Oop Lang'
>>> s="python is an oop lang.python is also fun lang"
>>> s.title()
'Python Is An Oop Lang.Python Is Also Fun Lang'
>>> s="PYTHON"
>>> s.title()
'Python'
>>> s="PYTHON"
>>> s.capitalize()
'Python'
>>>
>>>
>>> s="PyThOn"
>>> s.swapcase()
'pYtHoN'
>>> s="PYThon"
>>> s.swapcase()
'pytHON'
>>> s="PYTHON"
>>> s.swapcase()
'python'
>>> s="python"
>>> s.swapcase()
'PYTHON'
>>> s="12345"
>>> s.swapcase()
'12345'
>>> s="Python3.11"
>>> s.swapcase()
'pYTHON3.11'
>>> s="$%^&*()"
>>> s.swapcase()
'$%^&*()'
>>> s="PYTHON"
>>> s.lower()
'python'
>>> s="PYTHON"
>>> s.swapcase()
'python'
>>> s="PYThon"
>>> s.swapcase()
'pytHON'
>>> s.lower()
'python'
>>>
>>> s="python"
>>> s.lower()
'python'
>>> s.swapcase()
'PYTHON'
>>> s="python"
>>> s.upper()
'PYTHON'
>>> s="PYThon"
>>> s.upper()
'PYTHON'
>>> s="PYThon"
>>> s.lower()
'python'
>>>
>>> s="PYTHON"
>>> s.isupper()
True
>>> s="python"
>>> s.isupper()
False
>>> s="PYTHon"
>>> s.isupper()
False
>>> s="java"
>>> s.islower()
True
>>> s="JAva"
>>> s.islower()
False
>>> s.isupper()
False
>>> s="1234"
>>> s.islower()
False
>>> s.isupper()
False
>>>
>>>
>>> s="python"
>>> s.index('p')
0
>>> s.index('o')
4
>>> s.index('k')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s.index('2')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s="python"
>>> s.index('thon')
2
>>> s.index('khon')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s="python is an oop lang"
>>> s.index('is')
7
>>> s.index('o')
4
>>> s.index('an')
10
>>> s.index('10')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s.index("""an""")
10
>>> s="Apple"
>>> s.isalpha()
True
>>> s="Apple123"
>>> s.isalpha()
False
>>> s="Ap ple"
>>> s.isalpha()
False
>>> s="123"
>>> s.isalpha()
False
>>> s="Pyth$on"
>>> s.isalpha()
False
>>> s="PYTHON311"
>>> s.isalnum()
True
>>> s="PYTHON"
>>> s.isalnum()
True
>>> s="311"
>>> s.isalnum()
True
>>> s="PYT HON"
>>> s.isalnum()
False
>>> s="PYTHON3.11"
>>> s.isalnum()
False
>>> s="PYTH$on"
>>> s.isalnum()
False
>>> s="123.56"
>>> s.isalnum()
False
>>> s="123"
>>> s.isnumeric()
True
>>> s="123.45"
>>> s.isnumeric()
False
>>> s="123$23"
>>> s.isnumeric()
False
>>> s="2"
>>> s.isnumeric()
True
>>> s="32"
>>> s.isdigit()
True
>>> s="PYTHON311"
>>> s.isdigit()
False
>>> s=" "
>>> s.isspace()
True
>>> s="123 456"
>>> s.isspace()
False
>>> s=""
>>> s.isspace()
False
>>> s="   "
>>> s.isspace()
True
>>>
>>> s="Apple is in red"
>>> s.split()
['Apple', 'is', 'in', 'red']
>>> x=s.split()
>>> print(x,type(x))
['Apple', 'is', 'in', 'red'] <class 'list'>
>>> len(x)
4
>>> s="08-07-2023"
>>> print(s)
08-07-2023
>>> x=s.split("-")
>>> print(x)
['08', '07', '2023']
>>> print("Day=",x[0])
Day= 08
>>> print("Month=",x[1])
Month= 07
>>> print("Year=",x[2])
Year= 2023
>>> s="Apple#Mango#kiwi-Banana"
>>> print(s)
Apple#Mango#kiwi-Banana
>>> x=s.split("#")
>>> print(x)
['Apple', 'Mango', 'kiwi-Banana']
>>> y=s.split("-")
>>> print(y)
['Apple#Mango#kiwi', 'Banana']
>>> y[0]
'Apple#Mango#kiwi'
>>> y[0].split("#"]
  File "<stdin>", line 1
    y[0].split("#"]
                  ^
SyntaxError: closing parenthesis ']' does not match opening parenthesis '('
>>> y[0].split("#")
['Apple', 'Mango', 'kiwi']
>>> y[0:1]=y[0].split("#")
>>> print(y)
['Apple', 'Mango', 'kiwi', 'Banana']
>>>
>>> s="123$456$678$156$"
>>> print(s)
123$456$678$156$
>>> s.split("$")
['123', '456', '678', '156', '']
>>> s="123$456$678$156"
>>> s.split("$")
['123', '456', '678', '156']
>>>
>>>
>>>
>>> lst=["apple","mango","kiwi","guava"]
>>> print(lst,type(lst)
... )
['apple', 'mango', 'kiwi', 'guava'] <class 'list'>
>>> k=""
>>> k.join(lst)
'applemangokiwiguava'
>>> print(k)

>>> k
''
>>> lst=["apple","mango","kiwi","guava"]
>>> print(lst,type(lst))
['apple', 'mango', 'kiwi', 'guava'] <class 'list'>
>>> k=""
>>> k=k.join(lst)
>>> print(k)
applemangokiwiguava
>>> k
'applemangokiwiguava'
>>>
>>> lst=["apple","mango","kiwi","guava"]
>>> print(lst,type(lst))
['apple', 'mango', 'kiwi', 'guava'] <class 'list'>
>>> k=" "
>>> k=k.join(lst)
>>> print(k)
apple mango kiwi guava
>>> lst=["Python","is","an","oop","lang"]
>>> k=" "
>>> k=k.join(lst)
>>> print(k)
Python is an oop lang
>>> print(k,type(k))
Python is an oop lang <class 'str'>
>>> k.split()
['Python', 'is', 'an', 'oop', 'lang']
>>> s=" "
>>> s.isnull()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'str' object has no attribute 'isnull'
>>>
>>>
>>> s="Python is an oop lang"
>>> print(s)
Python is an oop lang
>>> s.startswith("Python")
True
>>> s.startswith("Pyt")
True
>>> s.startswith("p")
False
>>> s.startswith("p".upper())
True
>>> s.startswith("lang")
False
>>> s="Python is an oop lang"
>>> print(s)
Python is an oop lang
>>> s.endswith("Python")
False
>>> s.endswith("lang")
True
>>> s.endswith("la")
False
>>> s.endswith("ng")
True
>>> s.endswith("n")
False
>>> s.endswith("g")
True
>>> s.endswith("lang".upper())
False
>>>
















-------------------------------------------------------------------------------------------------------------------------------



				====================================
					String Handling Part-2
				====================================
=>On String Data, we can perform Indexing, Slicing Operations and with these operations, we can also perform different type of operations by using pre-defined functions present in str object.
--------------------------------------------------------------------------------------------------------------------------------
Pre-defined Functions in str object
--------------------------------------------------------------------------------------------------------------------------------
1) capitalize()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function is used for capitalizing the first letter First word of a given Sentence only.
=>Syntax:      strobj.capitalize()
				(OR)
			strobj=strobj.capitalize()
-----------------
Examples:
-----------------
>>> s="python"
>>> print(s,type(s))-------------------python <class 'str'>
>>> s.capitalize()--------------------'Python'
>>> s="python is an oop lang"
>>> print(s,type(s))-------------------------python is an oop lang <class 'str'>
>>> s.capitalize()-----------------------------'Python is an oop lang'
-------------------------------------
>>> s="python"
>>> print(s,type(s))--------------------python <class 'str'>
>>> s.capitalize()--------------------'Python'
>>> print(s,type(s))----------------python <class 'str'>
>>> s=s.capitalize()
>>> print(s,type(s))-----------------Python <class 'str'>
--------------------------------------------------------------------------------------------------------------------------------
2) title():
--------------------------------------------------------------------------------------------------------------------------------
=>This is used for obtaining Title Case of a Given Sentence  (OR) Making all words First 
    Letters are capital.
Syntax:          s.title()
			(OR)
			s=s.title()
	
------------------
Examples:
------------------
>>> s="python"
>>> print(s,type(s))-------------------python <class 'str'>
>>> s.capitalize()---------------------'Python'
>>> s.title()-----------------------------'Python'
----------------------------------------------------------
>>> s="python is an oop lang"
>>> print(s,type(s))------------------python is an oop lang <class 'str'>
>>> s.capitalize()--------------------'Python is an oop lang'
>>> s.title()----------------------------'Python Is An Oop Lang'
>>> print(s)----------------------------python is an oop lang
>>> s=s.title()
>>> print(s)--------------------------Python Is An Oop Lang
--------------------------------------------------------------------------------------------------------------------------------
3) index()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function obtains Index of the specified Value
=>If the specified value does not exist then we get ValueError
=>Syntax:        strobj.index(Value)
=>Syntax:	indexvalue=strobj.index(value)

Examples:
-----------------
>>> s="python"
>>> s.index("p")------------------0
>>> s.index("y")-------------------1
>>> s.index("o")-----------------4
>>> s.index("n")----------------5
>>> s.index("K")----------------ValueError: substring not found

--------------------------------------------------------------------------------------------------------------------------------
4) upper()
--------------------------------------------------------------------------------------------------------------------------------
=>It is used for converting any type of Str Data into Upper Case.
=>Syntax:-   strobj.upper()
			OR
			strobj=strobj.upper()
-----------------
Examples:
=---------------
>>> s="python"
>>> print(s)------------------------------python
>>> s.upper()-----------------------'PYTHON'
>>> s="python is an oop lang"
>>> print(s)---------------------------------python is an oop lang
>>> s.upper()--------------------------------'PYTHON IS AN OOP LANG'
>>> s="Python IS  an OOP lang"
>>> print(s)-------------------------------Python IS  an OOP lang
>>> s.upper()--------------------------'PYTHON IS  AN OOP LANG'
>>> s="AbCdEf"
>>> print(s)------------------------AbCdEf
>>> s.upper()----------------------'ABCDEF'
>>> s="PYTHON"
>>> print(s)--------------------PYTHON
>>> s.upper()-----------------'PYTHON'
>>> s="123"
>>> print(s)------------------123
>>> s.upper()----------------'123'
--------------------------------------------------------------------------------------------------------------------------------
5) lower()
--------------------------------------------------------------------------------------------------------------------------------
=>It is used for converting any type of Str Data into lower Case.
=>Syntax:-   strobj.lower()
			OR
			strobj=strobj.lower()
Examples:
-----------------
>>> s="Data Science"
>>> print(s)--------------Data Science
>>> s.lower()------------'data science'
>>> s="python"
>>> print(s)-------------python
>>> s.lower()-----------'python'
>>> s="PYTHON"
>>> print(s)-------------PYTHON
>>> s.lower()------------'python'
>>> s="PYThon"
>>> print(s)----------PYThon
>>> s.lower()---------'python'
--------------------------------------------------------------------------------------------------------------------------------
6) isupper()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided the given str object data is purely Upper Case otherwise it returns False.
Syntax:     strobj.isupper()

Examples:
-----------------
>>> s="PYTHON"
>>> s.isupper()-----------True
>>> s="python"
>>> s.isupper()----------False
>>> s="Python"
>>> s.isupper()----------False
>>> s="PYThon"
>>> s.isupper()----------False
>>> s="123"
>>> s.isupper()------------False
>>> s="%$#^&@"
>>> s.isupper()-----------False

--------------------------------------------------------------------------------------------------------------------------------
7)islower()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided the given str object data is purely lower Case otherwise it returns False.
	Syntax:     strobj.islower()
-----------------
Examples:
-----------------
>>> s="pythopn"
>>> s.islower()------------True
>>> s="pythOn"
>>> s.islower()------------False
>>> s="PYTHON"
>>> s.islower()-----------False
>>> s="123"
>>> s.islower()----------False
--------------------------------------------------------------------------------------------------------------------------------
8) isalpha()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided str object contains Purely Alphabets otherwise returns False.

		Syntax:   strobj.isalpha()
-------------------
Examples:
-------------------
>>> s="Ambition"
>>> s.isalpha()--------------------True
>>> s="Ambition123"
>>> s.isalpha()-------------------False
>>> s="1234"
>>> s.isalpha()------------------False
>>> s="   "
>>> s.isalpha()------------------False
>>> s="#$%^@"
>>> s.isalpha()-----------------False
>>> s="AaBbZz"
>>> s.isalpha()----------------True
--------------------------------------------------------------------------------------------------------------------------------
9) isdigit()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided given str object contains purely digits otherwise returns False
Examples:
--------------------
>>> s="python"
>>> s.isdigit()------------------False
>>> s="python123"
>>> s.isdigit()----------------False
>>> s="123"
>>> s.isdigit()-----------------True
>>> s="123 456"
>>> s.isdigit()---------------False
>>> s="1_2_3"
>>> s.isdigit()---------------False
>>> s="123KV"
>>> s.isdigit()-------------False
--------------------------------------------------------------------------------------------------------------------------------
10) isalnum()
--------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided str object contains either Alpabets OR Numerics or Alpha-Numerics only otherwise It returns False.
	=>Syntax:   strobj. isalphanum()
---------------------------
=>Examples:
---------------------------
>>> s="python310"
>>> s.isalnum()-----------------True
>>> s="python"
>>> s.isalnum()-----------------True
>>> s="310"
>>> s.isalnum()-----------------True
>>> s="$python310"
>>> s.isalnum()-----------------False
>>> s="python 310"
>>> s.isalnum()----------------False
>>> s="$python3.10"
>>> s.isalnum()----------------False
>>> s="python3.10"
>>> s.isalnum()-------------False
-------------------------------------------------------------------------------------------------------------------------------
11) isspace()
-------------------------------------------------------------------------------------------------------------------------------
=>This Function returns True provided str obj contains purely space otherwise it returns False.
=>Syntax:    strobj.isspace()
------------------------
Examples:
----------------------
>>> s="  "
>>> s.isspace()-----------True
>>> s=""
>>> s.isspace()--------------False
>>> s="python Prog"
>>> s.isspace()-------------False
>>> s="Prasana Laxmi"
>>> s.isspace()--------------False
>>> s.isalpha()-----------False
>>> s.isalpha() or s.isspace()-----------False
-------------------------------------------------------------------------------------------------------------------------------
12) split()
-------------------------------------------------------------------------------------------------------------------------------
=>This Function is used for splitting the given str object data into different words base specified delimter ( -  _  # % ^ ^ , ; ....etc)
=>The dafeult deleimter is space 
=>The Function returns Splitting data in the form of list object
=>Syntax:    strobj.split("Delimter")
				(OR)
			strobj.split()
				(OR)
			listobj=  strobj.split("Delimter")
				(OR)
			listobj=strobj.split()
----------------
Examples:
----------------
>>> s="Python is an oop lang"
>>> print(s)----------------Python is an oop lang
>>> s.split()----------------['Python', 'is', 'an', 'oop', 'lang']
>>> len(s.split())-----------5
>>> x=s.split()
>>> print(x,type(x))---------['Python', 'is', 'an', 'oop', 'lang'] <class 'list'>
>>> len(x)---------------5
>>> s="12-09-2022"
>>> print(s)-------------12-09-2022
>>> s.split("-")----------['12', '09', '2022']
>>> s="12-09-2022"
>>> dob=s.split("-")
>>> print(dob,type(dob))------------['12', '09', '2022'] <class 'list'>
>>> print("Day",dob[0])----------Day 12
>>> print("Month ",dob[1])---------Month  09
>>> print("Year ",dob[2])----------Year  2022
---------------------------------------------------------
>>> s="Apple#Banana#kiwi/Guava"
>>> words=s.split("#")
>>> print(words)-----------['Apple', 'Banana', 'kiwi/Guava']
>>> words=s.split("/")
>>> print(words)------------------['Apple#Banana#kiwi', 'Guava']
-------------------------------------------------------------------------------
13) join():
-------------------------------------------------------------------------------
=>This Function is used for combining or joining list of values from any Iterable object
=>Syntax:    strobj.join(Iterableobject)
Examples:
------------------------------
>>> lst=["HYD","BANG","AP","DELHI"]
>>> print(lst,type(lst))------------------['HYD', 'BANG', 'AP', 'DELHI'] <class 'list'>
>>> s=""
>>> s.join(lst)---------------'HYDBANGAPDELHI'
>>> s=" "
>>> s.join(lst)------------------'HYD BANG AP DELHI'
-------------------------------------------------------------------
>>> t=("Rossum","is", "Father" "of" ,"Python")
>>> print(t,type(t))
('Rossum', 'is', 'Fatherof', 'Python') <class 'tuple'>
>>> k=" "
>>> k.join(t)
'Rossum is Fatherof Python'
>>> t=("Rossum","is", "Father", "of" ,"Python")
>>> k=" "
>>> k.join(t)
'Rossum is Father of Python'
---------------------------------------------------------------------------------------------------------------------
14) startswith():
----------------------
=>The startswith() Function returns True if the string starts with the specified value, otherwise False.
Examples:
-------------------
>>>s="Python is an oop lang"
>>>s.startswith("Python")------------True
>>>s.startswith("python")------------False
---------------------------------------------------------------------------------------------------------------------
15) endswith():
----------------------
=>The endswith() Function returns True if the string ends with the specified value, otherwise False.
Examples:
-------------------
>>>s="Python is an oop lang"
>>>s.endswith("Python")------------False
>>>s.endswith("lang")------------True
---------------------------------------------------------------------------------------------------------------------
16) swapcase()
----------------------------
=>Make the lower case letters upper case and the upper case letters lower case:
Examples:
>>>s="PyThOn"
>>>s.swapcase()--------pYtHoN
---------------------------------------------------------------------------------------------------------------------
MISc Examples
---------------------------------------------------------------------------------------------------------------------
>>> s="python"
>>> s.capitalize()
'Python'
>>> s="python is an oop lang"
>>> s.capitalize()
'Python is an oop lang'
>>> s="python is an oop lang.python is also fun lang"
>>> s.capitalize()
'Python is an oop lang.python is also fun lang'
>>>
>>> s="python"
>>> s.title()
'Python'
>>> s="python is an oop lang"
>>> s.title()
'Python Is An Oop Lang'
>>> s="python is an oop lang.python is also fun lang"
>>> s.title()
'Python Is An Oop Lang.Python Is Also Fun Lang'
>>> s="PYTHON"
>>> s.title()
'Python'
>>> s="PYTHON"
>>> s.capitalize()
'Python'
>>>
>>>
>>> s="PyThOn"
>>> s.swapcase()
'pYtHoN'
>>> s="PYThon"
>>> s.swapcase()
'pytHON'
>>> s="PYTHON"
>>> s.swapcase()
'python'
>>> s="python"
>>> s.swapcase()
'PYTHON'
>>> s="12345"
>>> s.swapcase()
'12345'
>>> s="Python3.11"
>>> s.swapcase()
'pYTHON3.11'
>>> s="$%^&*()"
>>> s.swapcase()
'$%^&*()'
>>> s="PYTHON"
>>> s.lower()
'python'
>>> s="PYTHON"
>>> s.swapcase()
'python'
>>> s="PYThon"
>>> s.swapcase()
'pytHON'
>>> s.lower()
'python'
>>>
>>> s="python"
>>> s.lower()
'python'
>>> s.swapcase()
'PYTHON'
>>> s="python"
>>> s.upper()
'PYTHON'
>>> s="PYThon"
>>> s.upper()
'PYTHON'
>>> s="PYThon"
>>> s.lower()
'python'
>>>
>>> s="PYTHON"
>>> s.isupper()
True
>>> s="python"
>>> s.isupper()
False
>>> s="PYTHon"
>>> s.isupper()
False
>>> s="java"
>>> s.islower()
True
>>> s="JAva"
>>> s.islower()
False
>>> s.isupper()
False
>>> s="1234"
>>> s.islower()
False
>>> s.isupper()
False
>>>
>>>
>>> s="python"
>>> s.index('p')
0
>>> s.index('o')
4
>>> s.index('k')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s.index('2')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s="python"
>>> s.index('thon')
2
>>> s.index('khon')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s="python is an oop lang"
>>> s.index('is')
7
>>> s.index('o')
4
>>> s.index('an')
10
>>> s.index('10')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: substring not found
>>> s.index("""an""")
10
>>> s="Apple"
>>> s.isalpha()
True
>>> s="Apple123"
>>> s.isalpha()
False
>>> s="Ap ple"
>>> s.isalpha()
False
>>> s="123"
>>> s.isalpha()
False
>>> s="Pyth$on"
>>> s.isalpha()
False
>>> s="PYTHON311"
>>> s.isalnum()
True
>>> s="PYTHON"
>>> s.isalnum()
True
>>> s="311"
>>> s.isalnum()
True
>>> s="PYT HON"
>>> s.isalnum()
False
>>> s="PYTHON3.11"
>>> s.isalnum()
False
>>> s="PYTH$on"
>>> s.isalnum()
False
>>> s="123.56"
>>> s.isalnum()
False
>>> s="123"
>>> s.isnumeric()
True
>>> s="123.45"
>>> s.isnumeric()
False
>>> s="123$23"
>>> s.isnumeric()
False
>>> s="2"
>>> s.isnumeric()
True
>>> s="32"
>>> s.isdigit()
True
>>> s="PYTHON311"
>>> s.isdigit()
False
>>> s=" "
>>> s.isspace()
True
>>> s="123 456"
>>> s.isspace()
False
>>> s=""
>>> s.isspace()
False
>>> s="   "
>>> s.isspace()
True
>>>
>>> s="Apple is in red"
>>> s.split()
['Apple', 'is', 'in', 'red']
>>> x=s.split()
>>> print(x,type(x))
['Apple', 'is', 'in', 'red'] <class 'list'>
>>> len(x)
4
>>> s="08-07-2023"
>>> print(s)
08-07-2023
>>> x=s.split("-")
>>> print(x)
['08', '07', '2023']
>>> print("Day=",x[0])
Day= 08
>>> print("Month=",x[1])
Month= 07
>>> print("Year=",x[2])
Year= 2023
>>> s="Apple#Mango#kiwi-Banana"
>>> print(s)
Apple#Mango#kiwi-Banana
>>> x=s.split("#")
>>> print(x)
['Apple', 'Mango', 'kiwi-Banana']
>>> y=s.split("-")
>>> print(y)
['Apple#Mango#kiwi', 'Banana']
>>> y[0]
'Apple#Mango#kiwi'
>>> y[0].split("#"]
  File "<stdin>", line 1
    y[0].split("#"]
                  ^
SyntaxError: closing parenthesis ']' does not match opening parenthesis '('
>>> y[0].split("#")
['Apple', 'Mango', 'kiwi']
>>> y[0:1]=y[0].split("#")
>>> print(y)
['Apple', 'Mango', 'kiwi', 'Banana']
>>>
>>> s="123$456$678$156$"
>>> print(s)
123$456$678$156$
>>> s.split("$")
['123', '456', '678', '156', '']
>>> s="123$456$678$156"
>>> s.split("$")
['123', '456', '678', '156']
>>>
>>>
>>>
>>> lst=["apple","mango","kiwi","guava"]
>>> print(lst,type(lst)
... )
['apple', 'mango', 'kiwi', 'guava'] <class 'list'>
>>> k=""
>>> k.join(lst)
'applemangokiwiguava'
>>> print(k)

>>> k
''
>>> lst=["apple","mango","kiwi","guava"]
>>> print(lst,type(lst))
['apple', 'mango', 'kiwi', 'guava'] <class 'list'>
>>> k=""
>>> k=k.join(lst)
>>> print(k)
applemangokiwiguava
>>> k
'applemangokiwiguava'
>>>
>>> lst=["apple","mango","kiwi","guava"]
>>> print(lst,type(lst))
['apple', 'mango', 'kiwi', 'guava'] <class 'list'>
>>> k=" "
>>> k=k.join(lst)
>>> print(k)
apple mango kiwi guava
>>> lst=["Python","is","an","oop","lang"]
>>> k=" "
>>> k=k.join(lst)
>>> print(k)
Python is an oop lang
>>> print(k,type(k))
Python is an oop lang <class 'str'>
>>> k.split()
['Python', 'is', 'an', 'oop', 'lang']
>>> s=" "
>>> s.isnull()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'str' object has no attribute 'isnull'
>>>
>>>
>>> s="Python is an oop lang"
>>> print(s)
Python is an oop lang
>>> s.startswith("Python")
True
>>> s.startswith("Pyt")
True
>>> s.startswith("p")
False
>>> s.startswith("p".upper())
True
>>> s.startswith("lang")
False
>>> s="Python is an oop lang"
>>> print(s)
Python is an oop lang
>>> s.endswith("Python")
False
>>> s.endswith("lang")
True
>>> s.endswith("la")
False
>>> s.endswith("ng")
True
>>> s.endswith("n")
False
>>> s.endswith("g")
True
>>> s.endswith("lang".upper())
False
>>>