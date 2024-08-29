			=========================================================
					MemberShip Operators
			=========================================================
=>The purpose of MemberShip Operators is that "To Check the Existence of whether the value present in Iterable 
    Object or Not".
=>An Iterable Object is one which contains More than One Value such as Sequence Type(str,bytes,bytearray,range),List 
   Type (list, tuple), Set Type (set,frozenset) amd diict type (dict).
=>A Non-Iterable Object is one which contains One Value Only such as All Fundamental Types (int,float,bool,complex).
==>In Python Programming, we Two Types of Membership Operators. They are

				1. in Operator
				2. not in Operator
---------------------------------------------------------------------------------------------------------------------------------------------------
1. in Operator
---------------------------------------------------------------------------------------------------------------------------------------------------
Syntax:    Value in Iterable-Object
=>Here "in" Operator Returns True Provided Value present in Iterable-Object. 
=>Here "in" Operator Returns False Provided Value not present in Iterable-Object. 
---------------------------------------------------------------------------------------------------------------------------------------------------
2. not in Operator
---------------------------------------------------------------------------------------------------------------------------------------------------
Syntax:   value not in  Iterable-Object

=>Here "not in" Operator Returns True Provided Value not present in Iterable-Object. 
=>Here "not in" Operator Returns False Provided Value  present in Iterable-Object. 
---------------------------------------------------------------------------------------------------------------------------------------------------
Examples
---------------------------------------------------------------------------------------------------------------------------------------------------
>>> s="PYTHON"
>>> "P" in s------------------True
>>> "N" in s------------------True
>>> "K" not in s-------------True
>>> "K" in s------------------False
>>> "N" not in s-------------False
-----------------------------------------------
>>> s="PYTHON"
>>> "PYT" in s---------------------True
>>> "PYT" not in s---------------False
>>> "THO" in s-------------------True
>>> "THON" in s-----------------True
>>> "THON" not in s------------False
--------------------------------------------
>>> s="PYTHON"
>>> "PON" in s----------------------False
>>> "PTN" in s----------------------False
>>> "PTN" not in s-----------------True
>>> "PN" not in s-------------------True
>>> "PN" in s------------------------False
--------------------------------------------------
>>> s="PYTHON"
>>> "NOH" in s------------------False
>>> "NOH" not in s-------------True
>>> "NOH" in s[::-1]------------True
>>> "NOH" not in s[::-1]-------False
>>> "PN" not in s[::-1]----------True
>>> "NTP" not in s[::-2]--------True
>>> s[::-2]--------------------------'NHY'
>>> s[::2] in s--------------------False
>>> s[0:3] in s---------------------True
---------------------------------------------------------------------------------------------------------------------------------------------------
>>> lst=[10,"Rossum",45.67,2+4j]
>>> print(lst)---------------------[10, 'Rossum', 45.67, (2+4j)]
>>> 10 in lst----------------------True
>>> 2+4j not in lst---------------False
>>> "Rossum" not in lst--------False
>>> "Rossum" in lst-------------True
----------------------------------------
>>> lst=[10,"Rossum",45.67,2+4j]
>>> "Ros" in lst---------------False
>>> "Ros" in lst[1]------------True
>>> "Ros" not in lst[1]--------False
>>> "Rsum" not in lst[1]------True
>>> "Rsum" in lst[1]-----------False
-------------------------------------------------
>>> lst=[10,"Rossum",45.67,2+4j]
>>> print(lst)--------------------[10, 'Rossum', 45.67, (2+4j)]
>>> lst[1][0:3] in lst[1]-------True
>>> lst[1][0:5:2] not in lst[1]---------True
>>> lst[1][0:5:2] in lst[1]---------------False
-------------------------------------------------
>>> lst=[10,"Rossum",45.67,2+4j]
>>> print(lst)--------------------------[10, 'Rossum', 45.67, (2+4j)]
>>> 2+4j in lst-----------------------True
>>> 2+4j not in lst------------------False
>>> 2+4j in lst[-1]-----------------TypeError: argument of type 'complex' is not iterable
---------------------
>>> (2+4j).real in lst[-1].real------------TypeError: argument of type 'float' is not iterable
>>> (2+4j).imag not in lst[-1]-----TypeError: argument of type 'complex' is not iterable
---------------------------------------------------------------------------------------------------------------------------------------------------
>>> d1={10:"Python",20:"Java",30:"HTML"}
>>> print(d1,type(d1))------------------{10: 'Python', 20: 'Java', 30: 'HTML'} <class 'dict'>
>>> "Python" in d1----------------False
>>> "Python" in d1.values()----True
-------------------------------------------------------------------------------------------------------------------
>>> d1={10:"Python",20:"Java",30:"HTML"}
>>> print(d1,type(d1))---------------{10: 'Python', 20: 'Java', 30: 'HTML'} <class 'dict'>
>>> 10 in d1----------------------------True
>>> "Java" not in d1-----------------True
>>> "Java" not in d1[20]------------False
>>> "Java" in d1[20]-----------------True
>>> "Java" in d1.get(20)-------------True
>>> (10,"Python") in d1--------------False
>>> (10:"Python") in d1---------------SyntaxError: invalid syntax
>>> {10:"Python"} in d1---------------TypeError: unhashable type: 'dict'
>>> (10,"Python") in d1.items()------True
===================================================x======================================