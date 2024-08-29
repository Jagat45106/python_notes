	==========================================================================
		 Identity Operators----Applicable to Python Command Prompt
	==========================================================================
=>The Purpose of Identity Operators is that "To Compare Memory Address of Two Objects".
=>In Python Programming, we have 2 Identity Operators. They are

			1. is Operator
			2. is not Operator
---------------------------------------------------------------------------------------------------
1. is Operator
---------------------------------------------------------------------------------------------------
Syntax:     Object1  is  Object2
=>Here "is" Operator Returns True Provided Object1 and Object2 Contains Same address.
=>Here "is" Operator Returns False Provided Object1 and Object2 Contains Different address.
---------------------------------------------------------------------------------------------------
2. is not Operator
---------------------------------------------------------------------------------------------------
Syntax:     Object1  is not Object2
=>Here "is not" Operator Returns True Provided Object1 and Object2 Contains Different address.
=>Here "is" Operator Returns False Provided Object1 and Object2 Contains Same address.
-----------------------------------------------------------------------------------------------------------------------------------------------------------
NOTE1: a. When we apply "is" between Deep Copy objects  then we get True
       b. When we apply "is not " between Deep Copy objects  then we get False

NOTE2: a. When we apply "is" between Shallow Copy objects  then we get False
       b. When we apply "is not " between Shallow Copy objects  then we get True
---------------------------------------------------------------------------------------------------
Examples
---------------------------------------------------------------------------------------------------
>>> a=None
>>> b=None
>>> id(a)------------------140724091281872
>>> id(b)------------------140724091281872
>>> a is b-----------------True
>>> a is not b------------False
--------------------------------------------
>>> d1={10:"Apple",20:"Mango"}
>>> d2={10:"Apple",20:"Mango"}
>>> id(d1)
2096033953408
>>> id(d2)
2096033954048
>>> d1 is d2
False
>>> d1 is not d2
True
-------------------------------------------------
>>> s1={10,20,30}
>>> s2={10,20,30}
>>> print(s1,id(s1))-----------{10, 20, 30} 3005249268736
>>> print(s2,id(s2))-----------{10, 20, 30} 3005249271200
>>> s1 is s2-------------------False
>>> s1 is not s2---------------True
>>> fs1=frozenset({10,20,30})
>>> fs2=frozenset({10,20,30})
>>> print(fs1,id(fs1))----------frozenset({10, 20, 30}) 3005249270976
>>> print(fs2,id(fs2))----------frozenset({10, 20, 30}) 3005249926560
>>> fs1 is fs2-----------------False
>>> fs1 is not fs2-------------True
---------------------------------------------------
>>> lst1=[10,20,30,40]
>>> lst2=[10,20,30,40]
>>> print(lst1,id(lst1))
[10, 20, 30, 40] 3005246329216
>>> print(lst2,id(lst2))
[10, 20, 30, 40] 3005250703104
>>> lst1 is lst2
False
>>> lst1 is not lst2
True
>>> tpl1=(10,20,30,40,50)
>>> tpl2=(10,20,30,40,50)
>>> print(tpl1,id(tpl1))
(10, 20, 30, 40, 50) 3005249372224
>>> print(tpl2,id(tpl2))
(10, 20, 30, 40, 50) 3005249375424
>>> tpl1 is tpl2
False
>>> tpl1 is not tpl2
True
>>>-------------------------------------------------------------
>>> r1=range(10,21)
>>> r2=range(10,21)
>>> print(r1,type(r1),id(r1))
range(10, 21) <class 'range'> 3005249411552
>>> print(r2,type(r2),id(r2))
range(10, 21) <class 'range'> 3005250677488
>>> r1 is r2
False
>>> r1 is not r2
True
>>> ba1=bytearray([10,20,30])
>>> ba2=bytearray([10,20,30])
>>> print(ba1,type(ba1),id(ba1))
bytearray(b'\n\x14\x1e') <class 'bytearray'> 3005249393264
>>> print(ba2,type(ba2),id(ba2))
bytearray(b'\n\x14\x1e') <class 'bytearray'> 3005249304624
>>> ba1 is ba2
False
>>> ba1 is not ba2
True
>>> b1=bytes([10,20,30])
>>> b2=bytes([10,20,30])
>>> print(b1,type(b1),id(b1))
b'\n\x14\x1e' <class 'bytes'> 3005250677152
>>> print(b2,type(b2),id(b2))
b'\n\x14\x1e' <class 'bytes'> 3005250677104
>>> b1 is b2
False
>>> b1 is not b2
True
>>>------------------------------------
>>> s1="PYTHON"
>>> s2="PYTHON"
>>> print(s1,type(s1),id(s1))
PYTHON <class 'str'> 3005250677248
>>> print(s2,type(s2),id(s2))
PYTHON <class 'str'> 3005250677248
>>> s1 is s2
True
>>> s1 is not s2
False
>>> s1="THIS"
>>> s2="THIs"
>>> print(s1,type(s1),id(s1))
THIS <class 'str'> 3005250677392
>>> print(s2,type(s2),id(s2))
THIs <class 'str'> 3005250677200
>>> s1 is s2
False
>>> s1 is not s2
True

------------------------------------------------------------------------------------------------------------------
>>> a=2+3j
>>> b=2+3j
>>> print(a,type(a),id(a))
(2+3j) <class 'complex'> 3005249307120
>>> print(b,type(b),id(b))
(2+3j) <class 'complex'> 3005249321808
>>> a is b
False
>>> a is not b
True
>>>
--------------------------------------------------------------------------------------------------------------
>>> a=True
>>> b=True
>>> print(a,type(a),id(a))
True <class 'bool'> 140724961410704
>>> print(b,type(b),id(b))
True <class 'bool'> 140724961410704
>>> a is b
True
>>> a is not b
False
>>>
>>> a=1.2
>>> b=1.2
>>> print(a,type(a),id(a))
1.2 <class 'float'> 3005249307408
>>> print(b,type(b),id(b))
1.2 <class 'float'> 3005249307312
>>> a is b
False
>>> a is not b
True
>>>
------------------------------------
>>> a=300
>>> b=300
>>> print(a,type(a),id(a))
300 <class 'int'> 3005249307120
>>> print(b,type(b),id(b))
300 <class 'int'> 3005249322032
>>> a is b
False
>>> a is not b
True
>>> a=256
>>> b=256
>>> print(a,type(a),id(a))
256 <class 'int'> 140724962212248
>>> print(b,type(b),id(b))
256 <class 'int'> 140724962212248
>>> a is b
True
>>> a is not b
False
>>> a=0
>>> b=0
>>> print(a,type(a),id(a))
0 <class 'int'> 140724962204056
>>> print(b,type(b),id(b))
0 <class 'int'> 140724962204056
>>> a is b
True
>>> a is not b
False
>>>
>>>
>>> a=-1
>>> b=-1
>>> print(a,type(a),id(a))
-1 <class 'int'> 140724962204024
>>> print(b,type(b),id(b))
-1 <class 'int'> 140724962204024
>>> a is b
True
>>> a is not b
False
>>> a=-5
>>> b=-5
>>> print(a,type(a),id(a))
-5 <class 'int'> 140724962203896
>>> print(b,type(b),id(b))
-5 <class 'int'> 140724962203896
>>> a is b
True
>>> a is not b
False
>>> a=-6
>>> b=-6
>>> print(a,type(a),id(a))
-6 <class 'int'> 3005249322032
>>> print(b,type(b),id(b))
-6 <class 'int'> 3005249307120
>>> a is b
False
>>> a is not b
True
>>>-----------------------------------------------------
Multi Line assigment points
-----------------------------------------------------
>>> a,b=400,400
>>> print(a,type(a),id(a))
400 <class 'int'> 3005249321808
>>> print(b,type(b),id(b))
400 <class 'int'> 3005249321808
>>> a is b
True
>>> a is not b
False
>>> a,b=-400,-400
>>> print(a,type(a),id(a))
-400 <class 'int'> 3005249307120
>>> print(b,type(b),id(b))
-400 <class 'int'> 3005249307120
>>> a is b
True
>>> a is not b
False
>>> a,b=1.2,1.2
>>> print(a,type(a),id(a))
1.2 <class 'float'> 3005249307408
>>> print(b,type(b),id(b))
1.2 <class 'float'> 3005249307408
>>> a is b
True
>>> a is not b
False
>>> a,b=2+3j,2+3j
>>> print(a,type(a),id(a))
(2+3j) <class 'complex'> 3005249322064
>>> print(b,type(b),id(b))
(2+3j) <class 'complex'> 3005249322064
>>> a is b
True
>>> a is not b
False
>>>
>>>
>>> lst1,lst2=[10,20,30],[10,20,30]
>>> print(lst1,type(lst1),id(lst1))
[10, 20, 30] <class 'list'> 3005249305728
>>> print(lst2,type(lst2),id(lst2))
[10, 20, 30] <class 'list'> 3005250700608
>>> lst1 is lst2
False
>>> lst1 is not lst2
True
>>> d1,d2={10:"Apple"},{10:"Apple"}
>>> print(d1,type(d1),id(d1))
{10: 'Apple'} <class 'dict'> 3005249300736
>>> print(d2,type(d2),id(d2))
{10: 'Apple'} <class 'dict'> 3005249300480
>>> d1 is d2
False
>>> d1 is not d2
True
>>>