					========================================
						str handling  part-2
					========================================
=>Along with Indexing and Operations, we do many operations by using Pre-Defined Functions in str object.
--------------------------------------------------------------------------------------------------------------------------------------------------------

1) capitalize()
2) title()
3) swapcase()
4) lower()
5) upper()
6) count()
------------------------------
7) islower()
8) isupper()
9) isdigit()
10) isalpha()
11) isalnum()
------------------------------
12) split()   OR  split("delimeter")
13) join(Iterable Object)
----------------------------------------
14) index()
15) lstrip()
16) rstrip()
17) strip()
----------------------------------------
18) startswith()
19) endswith()
----------------------------------------------------------------------------------








Examples window on String handling-2

---------------------------------------------------------
capitalize() and title()
---------------------------------------------------------
>>> s="python"
>>> print(s)-------------------python
>>> s.capitalize()-----------'Python'
>>> print(s)-----------------python
>>> s="python"
>>> print(s)----------------python
>>> s=s.capitalize()
>>> print(s)
Python
>>>
>>>
>>> s="python"
>>> print(s)
python
>>> s.title()
'Python'
>>>
>>> s="python is an oop lang"
>>> print(s)
python is an oop lang
>>> s.capitalize()
'Python is an oop lang'
>>> print(s)
python is an oop lang
>>> s.title()
'Python Is An Oop Lang'
>>>
>>> s="Python IS AN OOP LANG"
>>> print(s)
Python IS AN OOP LANG
>>> s.capitalize()
'Python is an oop lang'
>>> s="Python IS AN OOP LANG"
>>> print(s)
Python IS AN OOP LANG
>>> s.title()
'Python Is An Oop Lang'
>>> s="python developed guio van rossum.python is an oop lang"
>>> print(s)
python developed guio van rossum.python is an oop lang
>>> s.capitalize()
'Python developed guio van rossum.python is an oop lang'
>>> print(s)
python developed guio van rossum.python is an oop lang
>>> s.title()
'Python Developed Guio Van Rossum.Python Is An Oop Lang'
----------------------------------------------------------------------------------------------------------------------
count()
----------------------------------------------------------------------------------------------------------------------
>>> s="MISSISSIPPI"
>>> print(s)---------------MISSISSIPPI
>>> s.count("M")
1
>>> s.count("S")
4
>>> s.count("P")
2
>>> s.count("I")
4
>>> s=123321456234123412
>>> print(s,type(s))--------123321456234123412 <class 'int'>
>>> s1=str(s)
>>> print(s1,type(s1))--------123321456234123412 <class 'str'>
>>> s1.count(1)--------------TypeError: must be str, not int
>>> s1.count('1')-----------4
>>> s1.count('2')-----------5
>>> s1.count(str(3))-------4
>>> len("MISSISSIPPI")------11
>>> "MISSISSIPPI".count("I")-----4
>>> s="123321456234123412"
>>> s.count("1")----------4
>>> len(s)-------------------18
-------------------------------------------------------------------------------
swapcase()
-------------------------------------------------------------------------------
>>> s="PyThOn"
>>> print(s)
PyThOn
>>> s.swapcase()
'pYtHoN'
>>> s="PYTHON"
>>> print(s)
PYTHON
>>> s.swapcase()
'python'
>>> s="python"
>>> print(s)
python
>>> s.swapcase()
'PYTHON'
>>> s="PYThon"
>>> print(s)
PYThon
>>> s.swapcase()
'pytHON'
>>> s="12345"
>>> print(s)
12345
>>> s.swapcase()
'12345'
>>> s="PyTHOn3.12"
>>> print(s)
PyTHOn3.12
>>> s.swapcase()
'pYthoN3.12'
------------------------------------------------------------------------------------------------------
upper() and lower()
-----------------------------------------------------------------------------------------------------
>>> s="python"
>>> print(s)
python
>>> s.upper()
'PYTHON'
>>> s="PYThon"
>>> print(s)
PYThon
>>> s.upper()
'PYTHON'
>>> print(s)
PYThon
>>> s.swapcase()
'pytHON'
>>>
>>> s="python"
>>> print(s)
python
>>> s.swapcase()
'PYTHON'
>>> print(s)
python
>>> s.upper()
'PYTHON'
>>> s="PYTHON"
>>> print(s)
PYTHON
>>> s.lower()
'python'
>>> print(s)
PYTHON
>>> s.swapcase()
'python'
>>> s="PYThon"
>>> print(s)
PYThon
>>> s.lower()
'python'
>>> print(s)
PYThon
>>> s.swapcase()
'pytHON'
----------------------------------------------------------------------------------------------
isupper() and islower()
----------------------------------------------------------------------------------------------
>>> s="PYTHON"
>>> print(s)
PYTHON
>>> s.isupper()
True
>>> s.islower()
False
>>> s="python"
>>> print(s)
python
>>> s.isupper()
False
>>> s.islower()
True
>>> s="PYThon"
>>> print(s)
PYThon
>>> s.isupper()
False
>>> s.islower()
False
>>> s="123#$%%"
>>> print(s)
123#$%%
>>> s.isupper()
False
>>> s.islower()
False
>>> s="P1234"
>>> print(s)
P1234
>>> s.isupper()
True
>>> s.islower()
False
>>> s="123p456"
>>> s.islower()
True
>>> s.isupper()
False
-------------------------------------------------------------------------------------------------------------
isdigit()
-------------------------------------------------------------------------------------------------------------
>>> s="123"
>>> print(s)
123
>>> s.isdigit()
True
>>> s="Python123"
>>> s.isdigit()
False
>>> s="12.34"
>>> s.isdigit()
False
-----------------------------------------------------------------------------------------------------------
isalpha()
----------------------------------------------------------------------------------------------------------
>>> s="python"
>>> print(s)------------python
>>> s.isalpha()-------True
>>> s="python3.10"
>>> s.isalpha()
False
>>> s="1234"
>>> s.isalpha()
False
>>> s="Python Prog"
>>> s.isalpha()
False
>>> s="Guido Van Rossum"
>>> s.isalpha()
False
-----------------------------------------------------------------------------
isalnum()
-----------------------------------------------------------------------------
>>> s="Python312"
>>> s.isalnum()
True
>>> s="123Java"
>>> s.isalnum()
True
>>> s="Python"
>>> s.isalnum()
True
>>> s="123"
>>> s.isalnum()
True
>>> s="Python3.12"
>>> s.isalnum()
False
>>> s="Python 312"
>>> s.isalnum()
False
-----------------------------------------------------------------------------------------------------------
isspace()
-----------------------------------------------------------------------------------------------------------
>>> s="    "
>>> s.isspace()
True
>>> s=""
>>> s.isspace()
False
>>> s="python 123"
>>> s.isspace()
False
>>> s="123 456 789"
>>> s.isspace()
False
----------------------------------------------------------------------------------------------------------
index()
----------------------------------------------------------------------------------------------------------
>>> s="PYTHON"
>>> s.index("P")
0
>>> s="RADAR"
>>> s.index("R")
0
>>> s="MISSISSIPPI"
>>> s.index("I")
1
>>> for ind,ch in enumerate(s):
...     print(ind,"--->",ch)
...
0 ---> M
1 ---> I
2 ---> S
3 ---> S
4 ---> I
5 ---> S
6 ---> S
7 ---> I
8 ---> P
9 ---> P
10 ---> I
>>> for ind,ch in enumerate(s):
...     if(ch=="I"):
...             print(ind,"--->",ch)
...
1 ---> I
4 ---> I
7 ---> I
10 ---> I
-------------------------------------------------------------------------------------------------------------------------------------------
split() and split("delimeter")
--------------------------------------------------------------------------------------------------------------------------------------------
>>> s="Python is an oop lang"
>>> x=s.split()
>>> print(x,type(x))
['Python', 'is', 'an', 'oop', 'lang'] <class 'list'>
>>> len(x)
5
>>> len(s)
21
>>> s="06-05-2024"
>>> x=s.split()
>>> print(x)
['06-05-2024']
>>> x=s.split("-")
>>> print(x)
['06', '05', '2024']
>>> print("DD=",x[0])
DD= 06
>>> print("MM=",x[1])
MM= 05
>>> print("YY=",x[2])
YY= 2024
>>> s="Apple#Mango-Kiwi#Guava"
>>> x=s.split("#")
>>> print(x)
['Apple', 'Mango-Kiwi', 'Guava']
>>> y=x[1].split("-")
>>> print(y)
['Mango', 'Kiwi']
>>> x[1]=y[0]
>>> print(x)
['Apple', 'Mango', 'Guava']
>>> x.insert(-1,y[1])
>>> print(x)
['Apple', 'Mango', 'Kiwi', 'Guava']
-----------------------------------------------------------------------------------------------------------------------------
join()
---------------------------------------------------------------------------------------------------------------------------------------
>>> lst=['PYTHON', 'IS', 'AN', 'FUN', 'PROG', 'LANG']
>>> print(lst,type(lst))
['PYTHON', 'IS', 'AN', 'FUN', 'PROG', 'LANG'] <class 'list'>
>>> s=" "
>>> s.join(lst)
'PYTHON IS AN FUN PROG LANG'
>>> print(s)

>>> s
' '
>>> lst=['PYTHON', 'IS', 'AN', 'FUN', 'PROG', 'LANG']
>>> print(lst,type(lst))
['PYTHON', 'IS', 'AN', 'FUN', 'PROG', 'LANG'] <class 'list'>
>>> s=" "
>>> s=s.join(lst)
>>> print(s)
PYTHON IS AN FUN PROG LANG
-----------------------------------------------------------------------------------------------------------------------
lstrip() , rstrip()  strip()
-----------------------------------------------------------------------------------------------------------------------------
>>> s="    Python"
>>> print(s,len(s))
    Python 10
>>> s=s.lstrip()
>>> print(s,len(s))
Python 6
>>> s="Python   "
>>> print(s,len(s))
Python    9
>>> s=s.rstrip()
>>> print(s,len(s))
Python 6
>>> s="   Python    "
>>> print(s,len(s))
   Python     13
>>> s=s.strip()
>>> print(s,len(s))
Python 6
--------------------
>>> s="Nirkar   Behra    "
>>> print(s,len(s))
Nirkar   Behra     18
>>> s=s.strip()
>>> print(s,len(s))
Nirkar   Behra 14
>>> " ".join(s.split())
'Nirkar Behra'
>>> s="++++++++++PYTHON++++++"
>>> s.strip("+")
'PYTHON'





