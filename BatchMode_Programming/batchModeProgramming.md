
---
**Batch Mode Programming**
---

**Number of Approaches to Develop Python Based Applications (OR) Programs**

---------------------------------
Definition of Program
---------------------------------
=>Set of Optimized Instructions developed by Programmer for Performing Certain Task is called Program.
=>The Optimized Instructions ate nothing but Taking Less time and Less Space to Execute the Program(Called Time 
    and Space Complexities).
=>The Purpose of Writing the Program for Performing Some Task Or Imeplementing Certain Operation.
---------------------------------
=>In Industry, we Types of Approaches to Develop Python Based Applications OR Programs, They are

			1. Interactive Approach
			2. Batch Mode Approach
-------------------------------------------------------------------------------------------------------------------------------------------------------------
1. Interactive Approach
-------------------------------------------------------------------------------------------------------------------------------------------------------------
=>In Interactive Approach, The Python Programmer Can Issue one Statement at a time and Obtains Result at a time for 
    that corresponding Statement.
=>Interactive Approach Most Useful to Test One Instruction at a Time.
=>Industry is not recommended to Use Interactive Approach bcoz of Two Reasons
			1. Not Able to Re-Use in Other Parts of Applications OR Projects
			2. Not Able to Provide a Facility to Save the Instructions.
-------------------------------
Examples Softwares:
-----------------------------
				a) Python Command Prompt
				b) Python IDLE Shell
=>The Above Softwares are automatically Installed when we Install Python Software.
-------------------------------------------------------------------------------------------------------------------------------------------------------------
2. Batch Mode Approach
-------------------------------------------------------------------------------------------------------------------------------------------------------------
=>In Batch Mode Approach, Python Programmer can develop Group of Instructions and Saved under One Single Unit 
    and that Corresponding Single Unit is Called File Name with Extenstion is called .py (FileName.py).
=>In real Time To Develop any project / Program / Application, we use only Batch Mode Approach.
=>The use of Batch Mode Approach is that "To Develop Group of Instructions, save them on file name with extension 
    .py (FileName.py) and Run that Application all at one".
-------------------------------
Examples Softwares:
-------------------------------
			1) Python IDLE Shell   (Comes along with Python Software)

	Industry always Recommends to Use Third Party IDEs. They are
	
					1. Pycharm
					2. Anconda Jupiter Note Book
					3. Anconda Spider
					4. VS Code
					5. Google Colab
					b. Sublime Text.................etc
NOTE:
------------
To Run the Python From Windows Command Prompt, we use Two Tools.
			1) python
			2) py
	=>Syntax1: E:\KVR-PYTHON-7AM\BATCH MODE>python FileName.py
	=>Syntax2: E:\KVR-PYTHON-7AM\BATCH MODE>py FileName.py
Examples
----------------
	=>Syntax1: E:\KVR-PYTHON-7AM\BATCH MODE>python sumex1.py
	=>Syntax2: E:\KVR-PYTHON-7AM\BATCH MODE>py  sumex2.py
NOTE: here "python" tool present in C:\Users\KVR\AppData\Local\Programs\Python\Python312     folder


#Write a Program for Cal Sum of Two Numbers
a=10
b=20
c=a+b
print(a)
print(b)
print(c)




#Program for Sum of Two Numbers
a=10
b=20
c=a+b
print("*"*40)
print("Val of a=",a)
print("Val of b=",b)
print("Sum=",c)
print("*"*40)


#Program for Adding of Two Numebrs
a=float(input("Enter First value:"))
b=float(input("Enter Second value:"))
c=a+b
print("*"*50)
print("Val of a=",a)
print("Val of b={}".format(b))
print("sum=",c)
print("*"*50)


**Display the Result of the Python Program on the Console**

=>To Display the Result of the Python Program on the Console, we use a Pre-Defined function called print().
=>In Otherwords, print() is used for displaying the Result of Python Program on the Console.
=>print() can be used in 6 Syntaxes. They are
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-1:		print(val1)
				OR
			print(val1,val2,....,val-n)
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>This Syntax is used for Displaying Either One Value or Multiple Values at a time on the console.
---------------------
Examples
---------------------
>>> a=10
>>> print(a)--------------10
>>> a=100
>>> b=200
>>> c=a+b
>>> print(a,b,c)-----------100 200 300
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-2:    print(msg1)
			OR
		    print(msg1,msg2,msg3.......,msg-n)
			OR
		    print(msg1+msg2+......+msg-n)
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>Here msg1,msg2,.....msg-n are calles String Data.
=>Here + is symbol used for Concatenating Two OR More Strings.
=>This Syntax display String Data.
---------------------------
Examples
---------------------------
>>> print("Hello Python")--------------Hello Python
>>> print("Hello",'python')-------------Hello python
>>> print("Hello"+"Python")-----------HelloPython
>>> print("Hello"+" "+"Python")-----Hello Python
>>> print("Python"+3.12)-----------TypeError: can only concatenate str (not "float") to str
>>> print("Python"+str(3.12))--------Python3.12
>>> print("Python",3.12)--------------Python 3.12
>>> print("Python","3.12")-------------Python 3.12
>>> print("Python"+" "+"3.12")-------Python 3.12
>>> print(2+3)------------------------------5
>>> print("2"+"3")-------------------------23
>>> print("2"+"3"+4)----------------------TypeError: can only concatenate str (not "int") to str
>>> print("2"+"3"+str(4))----------------234
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-3: print(Message cum Value)
			OR
		print(Value cum Message)
-----------------------------------------------------------------------------------------------------------------------------------------------------------
=>This Syntax display Values Cum Messages OR Messages Cum Values.
--------------------------
Examples
--------------------------
>>>a=10
>>> print("Val of a=",a)--------------Val of a= 10
>>> print("Val of a="+str(a))------Val of a=10
>>> a=10
>>> print(a,"is the val of a")----------10 is the val of a
>>> print(str(a)+" is the val of a")----10 is the val of a
---------------------------------------------------------------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum=",c)--------------sum= 30
>>> print(c,"is the sum")--------30 is the sum
>>> print("sum of ",a," and ",b,"=",c)----sum of  10  and  20 = 30
>>> print("Sum of "+str(a)+" and "+str(b)+"="+str(c))-----Sum of 10 and 20=30
----------------
>>> a=10
>>> b=20
>>> c=30
>>> d=a+b+c
>>> print("sum of ",a,",",b," and ",c,"=",d)-----------sum of  10 , 20  and  30 = 60
>>> print("Sum of "+str(a)+str(",")+str(b)+" and "+str(c)+str("=")+str(d))----Sum of 10,20 and 30=60
---------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum(",a,",",b,")=",c)-------------sum( 10 , 20 )= 30
>>> print("sum("+str(a)+str(",")+str(b)+str(")=")+str(c))-----------sum(10,20)=30
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-4:   print(Message cum Value with format() )
				(OR)
		   print(Value cum Message with format() )
-----------------------------------------------------------------------------------------------------------------------------------------------------------

--------------------------
Examples
--------------------------
>>> a=10
>>> print("Val of a={}".format(a))-------------Val of a=10
>>> print("{} is the val of a".format(a))-----10 is the val of a
---------------------------
>>> a=10
>>> print("Val of a={}".format(a))-----------Val of a=10
>>> print("{} is the val of a".format(a))----10 is the val of a
----------------------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum={}".format(c))------------sum=30
>>> print("sum of {} and {}={}".format(a,b,c))-----sum of 10 and 20=30
>>> print("sum({},{})={}".format(a,b,c))---------sum(10,20)=30
>>> a=10
>>> b=20
>>> c=30
>>> d=a+b+c
>>> print("sum of {},{} and {}={}".format(a,b,c,d))----sum of 10,20 and 30=60
				OR
>>> a=10
>>> print(f"val of a={a}")----------------val of a=10
--------------------
>>> a=10
>>> b=20
>>> c=a+b
>>> print(f"sum of {a},{b}={c}")-----------sum of 10,20=30
>>> print(f"sum({a},{b})={c}")-------------sum(10,20)=30
-----------------------------------------------------------------------------------------------------------------------------------------------------------
Syntax-5:    print(Message cum Value with format Specifiers)
-----------------------------------------------------------------------------------------------------------------------------------------------------------

=>Here Format Spefiers represents what type value we are displaying
=>Here %d Represents Integer Data
=>here %f Represents Floating Point Data.
=>here %s Represnts str data.
=>If any value does not contain Format Specifier then we must that Value into str type by using str() and use %s.
---------------------------
Examples
---------------------------
>>> a=10
>>> print("Val of a=%d" %a)------------Val of a=10
>>> a=10
>>> b=20
>>> c=a+b
>>> print("sum of %d and %d=%d" %(a,b,c))----sum of 10 and 20=30
>>> print("sum(%d,%d)=%d" %(a,b,c))-----sum(10,20)=30
>>> print("sum(%f,%f)=%f" %(a,b,c))----------sum(10.000000,20.000000)=30.000000
>>> print("sum(%0.2f,%0.2f)=%0.3f" %(a,b,c))----sum(10.00,20.00)=30.000
--------------------
>>> a=1.2
>>> b=2.3
>>> c=a+b
>>> print("sum(%f,%f)=%f" %(a,b,c))------------sum(1.200000,2.300000)=3.500000
>>> print("sum(%0.2f,%0.2f)=%0.3f" %(a,b,c))------sum(1.20,2.30)=3.500
>>> a=1.2
>>> b=2.3
>>> c=a+b
>>> print("sum(%f,%f)=%f" %(a,b,c))----------sum(1.200000,2.300000)=3.500000
>>> print("sum(%0.2f,%0.2f)=%0.3f" %(a,b,c))---sum(1.20,2.30)=3.500
>>> a=2.345678
>>> print("val of a=%f" %a)-----------val of a=2.345678
>>> print("val of a=%0.20f" %a)-----val of a=2.34567799999999992977
-----------------
>>> sno=10
>>> sname="Rossum"
>>> marks=3.4
>>> print("My Number is %d and Name is %s and Marks is %0.2f" %(sno,sname,marks))
			My Number is 10 and Name is Rossum and Marks is 3.40
>>> lst=[10,"Rossum",34.56]
>>> print("Content of lst={}".format(lst))-----------Content of lst=[10, 'Rossum', 34.56]
>>> print("Content of lst=%d" %lst)------------TypeError: %d format: a real number is required, not list
>>> print("Content of lst=%s" %str(lst))--------Content of lst=[10, 'Rossum', 34.56]